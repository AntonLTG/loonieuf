<script lang="ts">
  import { Button, Dropdown, DropdownItem, Chevron } from "flowbite-svelte";

  import Paymentcards from "./Paymentcards.svelte";

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
        <DropdownItem on:click={() => changeColor("Ljusgrå")}
          >Ljusgrå</DropdownItem
        >
        <DropdownItem on:click={() => changeColor("Mörkgrå")}
          >Mörkgrå</DropdownItem
        >
        <DropdownItem on:click={() => changeColor("Marin blå")}
          >Marin blå</DropdownItem
        >
        <DropdownItem on:click={() => changeColor("Bebis rosa")}
          >Bebis rosa</DropdownItem
        >
      </Dropdown>
    </div>
    <div class="buy-button-container">
      <a target="_blank" href="https://buy.stripe.com/5kA8zy6kN4uJcBG001">
        <div class="buy-button">Beställ nu</div>
      </a>
    </div>
    <div class="paymentcontainer">
      <Paymentcards />
    </div>

    <div class="description-title">Beskrivning</div>
    <div class="description">
      Vi presenterar Loonie Hoodie: Den här snygga och bekväma hoodien är
      tillverkad av ett mjukt, plyschigt tyg som håller dig varm och mysig även
      under de kyligaste nätterna. Den stora fickan ger dig gott om utrymme för
      att förvara saker som böcker, snacks eller till och med din telefon. Och
      den klassiska designen gör att den passar för alla tillfällen, oavsett om
      du slappar hemma eller en myskväll med vänner. Så om du letar efter ett
      sätt att hålla dig mysig och moderiktig när du kopplar av hemma, prova
      Blanket Hoodie idag!
    </div>

    <div class="bordercontainer">
      <div>Storleks Guide</div>
      <div>
        <div>Längd: xxx</div>
        <div>Midja: xxx</div>
        <div>Arm: xxx</div>
      </div>
    </div>

    <div class="bordercontainer">
      <div>Frakt</div>
      <div>YeS</div>
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
    font-family: "Noto Sans JP", sans-serif;

    padding-bottom: 1rem;
    border-bottom: 1px #eeeeee solid;
  }

  .bordercontainer {
    padding-bottom: 1rem;
    border-bottom: 1px #eeeeee solid;
  }

  .buy-button-container {
    display: flex;
    align-items: center;
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

  .paymentcontainer {
    border-bottom: 1px #eeeeee solid;
    padding-bottom: 1rem;
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
