<script lang="ts">
  import AiOutlineShopping from "svelte-icons-pack/ai/AiOutlineShopping";
  import Icon from "svelte-icons-pack/Icon.svelte";
  import Logo from "./../assets/img/Logo-loonieshop.png";
</script>

<div class="main">
  <div class="content-container">
    <img class="logo-img" src={Logo} alt="LoonieUFlogo" />
    <div class="titel">Loonie UF</div>
    <div class="shopping-bag">
      <Icon size="2rem" color="#EFF6EE" src={AiOutlineShopping} />
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
    width: 80vw;
    margin: auto;
  }

  .logo-img {
    width: 3rem;
  }

  .logo-img:hover {
    cursor: pointer;

    opacity: 80%;
  }

  .shopping-bag {
    border-radius: 2rem;
    padding: 0.2rem;
    transition: 800ms;
  }
  .shopping-bag:hover {
    background-color: #d4c2fc;
    cursor: pointer;
    scale: 110%;
    transition: 500ms;
  }

  .titel {
    font-family: "Stylish", sans-serif;
    font-size: 3rem;
    color: #d4c2fc;
    font-weight: bold;
  }

  .titel:hover {
    cursor: pointer;
    opacity: 80%;
  }
</style>
