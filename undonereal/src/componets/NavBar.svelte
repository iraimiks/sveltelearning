<script>
  import { Link } from "svelte-routing";
    let mobileNav = false; 
    function toggle(){
        mobileNav = !mobileNav;
    }
</script>

<style>
  .navbar {
    display: flex;
    background-color: rgb(251, 255, 0);
    color: #ce0000;
    padding: 16px;
    font-family: sans-serif;
  }
  .navbar-items {
    display: flex;
  }
  .navbar-link {
    padding-right: 8px;
  }
  .navbar-items-right {
    margin-left: auto;
  }
  .navbar-link-toogle {
    display: none;
  }
  .navbar-items-mobile{
      display: none;
  }
  @media only screen and (max-width: 768px) {
    .navbar, .navbar-items-mobile {
      flex-direction: column;
    }
    .navbar-items {
        display: none;
    }
    .navbar-items-mobile {
        display: flex;
    }
    .navbar-items-right {
      margin-left: 0;
    }
    .navbar-link-toogle {
      align-self: flex-end;
      display: initial;
      position: absolute;
      cursor: pointer;
    }
  }
</style>

<div class="navbar">
  <div class="navbar-link navbar-linkLogo">Her Logo</div>
  <div class="navbar-link navbar-link-toogle">
    <buttom on:click={toggle}><i class="fa fa-bars" aria-hidden="true" /></buttom>
  </div>
  <nav class="navbar-items navbar-items-right">
    <div class="navbar-link">
      <Link to="/">Home</Link>
    </div>
    <div class="navbar-link">
      <Link to="/creatproject" />
    </div>
    <div class="navbar-link">
      <Link to="/up">Up</Link>
    </div>
    <div class="navbar-link">
      <Link to="/userpage">User Place</Link>
    </div>
  </nav>
  {#if mobileNav}
  <nav class="navbar-items-mobile navbar-items-right">
    <div class="navbar-link">
      <Link to="/">Home</Link>
    </div>
    <div class="navbar-link">
      <Link to="/creatproject" />
    </div>
    <div class="navbar-link">
      <Link to="/up">Up</Link>
    </div>
    <div class="navbar-link">
      <Link to="/userpage">User Place</Link>
    </div>
  </nav>
  {:else}
    <div></div>
  {/if}
</div>
