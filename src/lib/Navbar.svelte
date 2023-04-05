<script lang="ts">
  import { Router, Link, Route } from "svelte-navigator";
  import Logo from "./../assets/img/Logo-loonieshop.png";
</script>

<div id="sticky-navbar">
  <div class="navbar">
    <div class="content-container">
      <Link to="/">
        <img class="logo-img" src={Logo} alt="LoonieUFlogo" />
      </Link>
      <Link to="/">
        <div class="titel">Loonie UF</div>
      </Link>

      <div class="shopping-bag" />
    </div>
  </div>
</div>

<style>
  #sticky-navbar {
    position: sticky;
    top: 0;
    width: 100%;
    z-index: 100;
  }
  .navbar {
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
