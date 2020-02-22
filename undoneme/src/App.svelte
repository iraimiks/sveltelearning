<script>
  import NavBar from "./components/navbar/NavBar.svelte";
  import { Router, Route } from "svelte-routing";
  import FormProjects from "./pages/FormProjects.svelte";
  import Home from "./pages/Home.svelte";
  import TestingStore from "./pages/TestingStore.svelte"
  export let url = "";
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
      <Route path="/create">
        <FormProjects />
      </Route>
      <Route path="/test">
        <TestingStore />
      </Route>
    </div>
  </Router>

</main>
