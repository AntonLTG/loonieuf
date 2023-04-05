<script lang="ts">
  import Page1 from "./lib/Page1.svelte"
  import Page2 from "./lib/Page2.svelte"
  import Page3 from "./lib/Page3.svelte"
  import Page4 from "./lib/Page4.svelte"
  import Page5 from "./lib/Page5.svelte"
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
    <div class="content">
      <Route path="/">
        <Page1 />
      </Route>

      <Route path="/betalningsmetoder">
        <Page2 />
      </Route>

      <Route path="/om-oss">
        <Page3 />
      </Route>
      
      <Route path="/privacy">
        <Page4/>
      </Route>
      
      <Route path="/terms">
        <Page5 />
      </Route>
    </div>
    <CustomFooter/>
  </Router>
</main>

<style>
  .content{
    display: flex;
    justify-content: center;
  }
</style>
