<script lang="ts">
  import Navbar from "./Navbar.svelte";
  import PaymentCard from "./PaymentCard.svelte";
</script>



<main>
  <Navbar />
  <PaymentCard/>
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: auto;
  }
</style>
