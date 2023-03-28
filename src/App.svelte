<script lang="ts">
  import MainCard from "./lib/MainCard.svelte";
  import Navbar from "./lib/Navbar.svelte";
  import Logo from "././assets/img/Logo-loonieshop.png";
</script>

<svelte:head>
  <link rel="icon" type="image/svg" href={Logo} />
</svelte:head>

<main>
  <div id="sticky-navbar">
    <Navbar />
  </div>
  <MainCard />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: auto;
  }
  #sticky-navbar {
    position: sticky;
    top: 0;
    width: 100%;
  }
</style>
