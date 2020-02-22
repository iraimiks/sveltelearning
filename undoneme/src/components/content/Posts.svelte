<script>
  import { onMount } from "svelte";

  const apiBaseUrl =
    "https://ndb99xkpdk.execute-api.eu-west-2.amazonaws.com/dev";
  let posts = [];

  onMount(async () => {
    const res = await fetch(apiBaseUrl + "/posts");
    posts = await res.json();
  });

  function editPost(post){
    console.log(post);
  }
  function deletePost(id){
    console.log('Deleted post id is '+id);
  }
</script>

<style>
  .row-post {
    display: flex;
     flex-flow: row wrap;
  }
  .col-post {
     width: 200px;
     margin: 10px;
  }
</style>

<div class="row-post">
    {#if posts.length === 0}
      <h3>Loading...</h3>
    {:else}
      {#each posts as post}
        <div class="col-post">
          <div>
            <h1>{post.title}</h1>
            <p>{post.createAt}</p>
            <p>{post.body}</p>
          </div>
          <button on:click={() => editPost(post)}>Edit</button>
          <button on:click={() => deletePost(post.id)}>Delete</button>
        </div>
      {/each}
    {/if}
</div>
