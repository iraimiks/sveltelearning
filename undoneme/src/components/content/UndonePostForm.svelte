<script>
    import { createEventDispatcher } from 'svelte';


    import { setContext } from 'svelte';
    import { Link } from "svelte-routing";
    const dispatch = createEventDispatcher();
    let textForm = '';
    const submit = () => dispatch('submit');
    let text = [];
    function onSubmit(event){
        event.preventDefault();
        text = [...text, textForm];
    }
    
</script>

<style>

</style>
<div>{text}</div>
<form on:submit={onSubmit}>
    <div>
        <lable for="title">Title</lable>
        <input type="text" name="title">
    </div>
    <div>
        <lable for="description">Description</lable>
        <textarea id="description" name="description" ></textarea>
    </div>
    <div>
        <lable for="github">GitHub</lable>
        <input type="text" name="github" bind:value={textForm}>
    </div>
    <button on:click={submit} >Add</button>
    <Link to="/"><button>Go to project</button></Link>
</form>