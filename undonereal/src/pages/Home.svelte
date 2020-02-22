<script>
    import { posts } from '../store.js';



</script>
<ul>
	{#each $posts as form}
		<li>{form.title}</li>	
	{:else}
	<p>
	   Add your post
	</p>
	{/each}
</ul>