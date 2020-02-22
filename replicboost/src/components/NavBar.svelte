<script>
  import { link } from "svelte-routing";
  let mobileNav = false;
  function toggle() {
    mobileNav = !mobileNav;
  }
</script>

<style>
  .navbar {
    display: flex;
    color: #ce0000;
    padding: 0em 2em 0 2em;
    font-family: sans-serif;
    top: 30px;
    font-size: 1.2rem;
    font-weight: 550;
  }
  .navbar-items {
    display: flex;
  }
  .navbar-link {
    padding-right: 0.1em;
  }
  .navbar-items-right {
    margin-left: auto;
  }
  .navbar-link-toogle {
    display: none;
  }
  .navbar-items-mobile {
    display: none;
  }
  .style-nav-anc {
    padding: 8px 8px 8px 32px;
    color: #222222;
    transition: 0.3s;
  }
  .style-nav-anc:hover {
    color: #960101;
  }
  @media only screen and (max-width: 768px) {
    .navbar,
    .navbar-items-mobile {
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
  <div class="navbar-link navbar-linkLogo">Logo te</div>
  <div class="navbar-link navbar-link-toogle">
    <buttom on:click={toggle}>
      <i class="material-icons">menu</i>
    </buttom>
  </div>
  <nav class="navbar-items navbar-items-right">
    <div>
      <a class="style-nav-anc" href="/" use:link>SAKUMS</a>
    </div>
    <div class="navbar-link">
      <a class="style-nav-anc" href="/up"  use:link>SERVICE</a>
    </div>
    <div class="navbar-link">
      <a class="style-nav-anc" href="/userpage" use:link>TŪNINGS</a>
    </div>
    <div class="navbar-link">
      <a class="style-nav-anc" href="/userpage" use:link>KONTAKTI</a>
    </div>
    <div class="navbar-link style-nav-anc">
      <select>
        <option value="0">LV</option>
        <option value="1">RU</option>
        <option value="2">ENG</option>
      </select>
    </div>
  </nav>
  {#if mobileNav}
    <nav class="navbar-items-mobile navbar-items-right">
      <div class="navbar-link">
        <a href="/" use:link>Home</a>
      </div>
      <div class="navbar-link">
        <a href="/up" use:link>Up</a>
      </div>
      <div class="navbar-link">
        <a href="/userpage">User Place</a>
      </div>
    </nav>
  {:else}
    <div />
  {/if}
</div>
