<script>
  import { Router, Route } from "svelte-routing";
  import Home from "./pages/Home.svelte";
  import NavBar from "./components/NavBar.svelte";
  import Footer from "./components/Footer.svelte";
  let url = "";
</script>

<style>
  .nav-bar-rel {
    width: 100%;
    position: absolute;
    z-index: 34;
    top: 30px;
    height: 90px;
  }
</style>

<main>
  <Router {url}>
    <div class="nav-bar-rel">
      <NavBar />
    </div>
      <Route path="/">
        <Home />
      </Route>
      <Footer />
  </Router>
</main>
