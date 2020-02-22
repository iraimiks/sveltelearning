<script>
    import { userName } from '../store.js';
    let user = '';
    let userFromStore = $userName;
</script>
<h2>{ user }</h2>
<input type="text" bind:value={user}>
<button on:click={userName.set(user)}>ADd</button>

<h2>{userFromStore}</h2>