<script>
    let posts = [];
    let postTitle = '';
    let postDescription = '';
    let i = 0;

    function create() {
        posts = posts.concat({ postTitle, postDescription});
        i = postDescription.length - 1;
        postTitle = '';
        postDescription = '';
    }

    function update(){
        posts[i] = { postTitle, postDescription}
    }

    function remove(){
        posts = [...posts.slice(0, i), ...posts.slice(i+1)];
        postTitle = '';
        postDescription = '';
        i = Math.min(i, posts.length - 1);
    }
</script>

<div>
    {#each posts as post}
        <div>{post.postTitle}</div>
        <div>{post.postDescription}</div>
    {/each}
</div>

<lable>
<input bind:value={postTitle}>
</lable>
<lable>
<input bind:value={postDescription}>
</lable>

<div>
    <button on:click={create} disabled="{!postTitle || !postDescription}">create</button>
    <button on:click={remove} disabled="{!postTitle || !postDescription}">delete</button>

</div>