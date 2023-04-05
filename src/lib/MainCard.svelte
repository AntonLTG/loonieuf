<script lang="ts">
  import { Button, Dropdown, DropdownItem, Chevron } from "flowbite-svelte";

  // ./imageData/+server.js has the following

  import CustomCarousel from "./PhotoCollection/CustomCarousel.svelte";
  import type { ColorTypes } from "./PhotoCollection/types";

  let dropdownOpen = false;
  let currentColor: ColorTypes = "Ljusgrå";

  const changeColor = (color: ColorTypes) => {
    dropdownOpen = false;
    currentColor = color;
  };
</script>

<div class="mainCard">
  <div class="vRuta">
    <div class="laCarousel">
      <CustomCarousel picColor={currentColor} />
    </div>
  </div>
  <div class="hRuta">
    <div class="Title">Loonie Hoodie</div>
    <div class="pris">Pris: 399 Kr</div>
    <div class="storlek">Storlek: One Size</div>
    <div class="pris">
      <Button color="light">
        <Chevron>{currentColor}</Chevron>
      </Button>
      <Dropdown bind:open={dropdownOpen}>
        <DropdownItem on:click={() => changeColor("Ljusgrå")}>Ljusgrå</DropdownItem>
        <DropdownItem on:click={() => changeColor("Mörkgrå")}>Mörkgrå</DropdownItem>
        <DropdownItem on:click={() => changeColor("Marin blå")}>Marin blå</DropdownItem>
        <DropdownItem on:click={() => changeColor("Bebis rosa")}>Bebis rosa</DropdownItem>
      </Dropdown>
    </div>
    <div class="buy-button-container">
      <a target="_blank" href="https://buy.stripe.com/5kA8zy6kN4uJcBG001">
        <div class="buy-button">Beställ nu</div>
      </a>
    </div>
    <div class="description-title">Beskrivning</div>
    <div class="description">
      Lorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem
      ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum
      dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit
      ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem
      ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum
      dolor sit ametLorem ipsum dolor sit amet
    </div>
  </div>
</div>

<style>
  @media screen and (min-width: 850px) {
    .mainCard {
      display: flex;
      padding-top: 20vh;
    }
    .Title {
      border-top: 0px #eeeeee solid;
    }
  }

  .mainCard {
    width: 80vw;
    background-color: white;
    padding: 3rem;
    padding-top: 0rem;
    padding-bottom: 10rem;
    gap: 5rem;
  }

  .Title {
    display: flex;
    justify-content: center;
    height: 10%;
    font-size: 3rem;
    font-family: "Oswald", sans-serif;
    margin-bottom: 2rem;
    margin-top: 9vh;
    border-bottom: 1px #eeeeee solid;
    border-top: 1px #eeeeee solid;
  }

  .pris {
    font-family: "Oswald", sans-serif;
    font-weight: bold;
    font-size: 1.4rem;
  }

  .storlek {
    font-family: "Oswald", sans-serif;
    font-weight: bold;
    font-size: 1.4rem;
  }

  .laCarousel {
    border-bottom: 1px #eeeeee solid;
    padding-bottom: 2vh;
  }
  .vRuta,
  .hRuta {
    flex: 1;
  }

  .hRuta {
    gap: 1rem;
    flex-direction: column;
    display: flex;
  }

  .description-title {
    text-decoration: underline;
    font-family: "Oswald", sans-serif;
    font-weight: bold;
    font-size: 1.4rem;
    margin-top: 1vh;
  }
  .description {
    padding-bottom: 1rem;
    border-bottom: 1px #eeeeee solid;
  }

  .buy-button-container {
    display: flex;
    align-items: center;
    border-bottom: 1px #eeeeee solid;
    padding-bottom: 1rem;
  }

  .buy-button {
    align-items: center;
    display: flex;
    justify-content: center;
    padding: 0.5rem;
    width: 10rem;
    background: #1d3461;
    border-radius: 7px;
    color: #ffff;
    transition: 1000ms;
    font-family: "Montserrat", sans-serif;
    font-size: 1.1rem;
    letter-spacing: 1px;
  }

  .buy-button:hover {
    background: #2a4b8d;
    transition: 400ms;
    scale: 101%;
    cursor: pointer;
  }

  /* ________________________vänster ruta_____________ */

  .vRuta {
    display: flex;
    justify-content: center;
    flex-direction: column;
  }

  /*{
    border-style: solid;
    border-color: red;
    border-width: 4px;
}*/
</style>
