<script>
  import { Link } from "svelte-routing";
  import LoginBtn from "./buttons/LoginBtn.svelte";
  import SingUpBtn from "./buttons/SingUpBtn.svelte";
  import AccBtn from "./buttons/AccBtn.svelte";
  import CreateProject from "./buttons/CreateProject.svelte";
</script>

<style>
  .box-nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    background: #1290c273;
  }
  .ul-nav {
    display: flex;
    flex-direction: row;
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
  }
  .li-nav {
    display: block;
    color: black;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
  }
</style>

<div class="box-nav">
  <div>
    <div><Link to="/">Logo</Link></div>
  </div>
  <div>
    <ul class="ul-nav">
      <li class="li-nav">
        <LoginBtn />
      </li>
      <li class="li-nav"><SingUpBtn /></li>
      <li class="li-nav"><Link to="/create"><CreateProject /></Link></li>
      <li class="li-nav"><AccBtn /></li>
      <li class="li-nav"><Link to="/test"><CreateProject /></Link></li>
      <li class="li-nav" />
    </ul>
  </div>
</div>
