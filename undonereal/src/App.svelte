<script>
	import { Router, Route } from "svelte-routing";
	import NavBar from "./componets/NavBar.svelte";
	import Home from "./pages/Home.svelte";
	import UserPage from "./pages/UserPage.svelte";
	let url = "";
</script>
<style>
	
</style>
<main>
<Router {url}>
    <NavBar />
    <div>
      <Route path="/">
        <Home />
      </Route>
	  <Route path="/userpage">
        <UserPage />
      </Route>
    </div>
  </Router>
</main>
