<script lang="ts">
  import AiOutlineShopping from "svelte-icons-pack/ai/AiOutlineShopping";
  import Icon from 'svelte-icons-pack/Icon.svelte';

</script>

<div class="main">
  <div class="content-container">
    <img
      class="logo-img"
      src="assets\img\Logo-loonieshop.png"
      alt="LoonieUFlogo"
    />
    <div class="titel">Loonie UF</div>
    <div class="shopping-bag"><Icon size="2rem" color="#EFF6EE" src={AiOutlineShopping} />
    </div>
  </div>
</div>

<style>
  .main {
    background: #1f487e;
    width: 100vw;
  }

  .content-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.5rem;
    }
  
  .logo-img {
    width: 3rem;
    margin-left: 12rem;
  }
  
  .logo-img:hover{
    cursor: pointer;
    opacity: 80%;
  }

  .shopping-bag{
    margin-right: 12rem;
    border-radius: 2rem;
    padding: 0.2rem;
  }
  .shopping-bag:hover{
    background-color: #D4C2FC;
    cursor: pointer;
    scale: 110%;
    transition: 500ms;
  }

  .titel {
    font-family: "Stylish", sans-serif;
    font-size: 3rem;
    color: #D4C2FC;
    font-weight: bold;
  }

  .titel:hover{
    cursor: pointer;
    opacity: 80%;  }

</style>
