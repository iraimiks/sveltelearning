<script>
    import Posts from '../components/content/Posts.svelte';
    import CrudLearn from '../components/content/LearnCrud.svelte';
    import UndonePostForm from '../components/content/UndonePostForm.svelte';
  //  import UndonePostForm from '../components/content/UndonePostForm.svelte';
    function sum(x, y, z){
        return x+y+z;
    }

    let num = 0;
    let sumNum = 0;
    let numbers = [];
    function addNumber(){
        numbers = [...numbers, num];
    }
    function sumAll(){
        numbers.forEach(n => { sumNum += n})
    }
    function reset(){
        numbers = [];
    }
  
    console.log(sum(...numbers));
    console.log(num);
</script>

<style>
    .container-home {
        width: 90%;
        margin: 0 auto;
    }
</style>
<div class="container-home">
<h2>Test input numbers</h2>
    <!-- <h2>Input numbers: {numbers}</h2>
    <h3>Masive number sum is : {sumNum}</h3>
    <input type="number" bind:value="{num}">
    <button on:click="{addNumber}" >Add numbe</button>
    <button on:click="{sumAll}" >Sum num</button>
    <button on:clock="{reset}">Reset input</button> -->
    <!-- <Posts /> -->
    <!-- <CrudLearn /> -->
    <h2><UndonePostForm on:submit/></h2>
</div>

