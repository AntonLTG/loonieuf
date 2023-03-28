<script lang="ts">
  import MainCard from "./lib/MainCard.svelte";
  import Navbar from "./lib/Navbar.svelte";
  import Logo from "././assets/img/Logo-loonieshop.png";
</script>

<svelte:head>
  <link rel="icon" type="image/svg" href={Logo} />
</svelte:head>

<main>
  <Navbar />
  <MainCard />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: auto;
  }
</style>
