<script>
    import { posts } from '../store.js';

    let formPost = [];
    let title = '';
    function addPost(){
        const newPost = {
            title
        };
        formPost = formPost.concat(newPost);
        posts.set(formPost);
    }
</script>

<style>

</style>

<div>
    <label for="title">Title</label>
	<input type="text" id="title" bind:value={title}/>
</div>
<button on:click={addPost}>ADD Book</button>

