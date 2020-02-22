<script>
    export let count = 0;
    function countMy(){
      count += 1;
    }
</script>

    <button on:click="{countMy}">count: {count}</button>
