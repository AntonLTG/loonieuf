<script lang="ts">
    import MainCard from "./lib/MainCard.svelte";
    import Navbar from "./lib/Navbar.svelte";
</script>

<main>
  <Navbar/>
  <MainCard/>

</main>

<style>
  main{
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
