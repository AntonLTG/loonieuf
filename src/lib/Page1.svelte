<script lang="ts">
  import MainCard from "./MainCard.svelte";
  import Navbar from "./Navbar.svelte";
</script>



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
