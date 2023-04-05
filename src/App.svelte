<script lang="ts">
  import Page1 from "./lib/Page1.svelte";
  import Page2 from "./lib/Page2.svelte"
  import Logo from "./assets/img/Logo-loonieshop.png"
  import { Router, Link, Route } from "svelte-navigator";
  import Navbar from "./lib/Navbar.svelte";
  import CustomFooter from "./lib/Footer.svelte"

  </script>  



<svelte:head>
  <link rel="icon" type="image/svg" href={Logo} />
</svelte:head>

<main>
  <Router>
      <Navbar/>
    <div>
      <Route path="/">
        <Page1 />
      </Route>
      <Route path="/checkout">


        <Route path="/">
          <Page2 />
        </Route>
        <Route path="/completed">
          <Page2 />
        </Route>


      </Route>
    </div>
  </Router>
  <CustomFooter/>
</main>

<style>

</style>
