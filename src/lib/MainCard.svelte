<script lang="ts">
  import blankethoodiegirl from "./../assets/img/blankethoodie.png";
  import Logo from "./../assets/img/Logo-loonieshop.png";
  import { Button, Dropdown, DropdownItem, Chevron } from 'flowbite-svelte'

  import { CarouselTransition } from "flowbite-svelte";
  // ./imageData/+server.js has the following
  export const images = [
    {
      id: 0,
      name: "Cosmic timetraveler",
      imgurl: blankethoodiegirl,
    },
    {
      id: 1,
      name: "Cosmic timetraveler",
      imgurl: Logo,
    },
  ];
</script>

<div class="mainCard">
  <div class="vRuta">
    <div>
      <CarouselTransition
        {images}
        transitionType="fly"
        transitionParams={{ delay: 250, duration: 300 }}
        showCaptions={false}
        showThumbs={false}
      />
    </div>
  </div>
  <div class="hRuta">
    <div class="Title">Loonie Hoodie</div>
    <div class="pris">Pris: 399 Kr</div>
    <div class="storlek">Storlek: One Size</div>
    <div class="pris">
      <Button><Chevron>Färg</Chevron></Button>
      <Dropdown >
        <DropdownItem>Grå</DropdownItem>
      </Dropdown>
    </div>
    <div class="buy-button-container">
      <a href="https://buy.stripe.com/5kA8zy6kN4uJcBG001"
      ><div class="buy-button">Beställ nu</div></a
      >
    </div>
    <div class="description-title">Beskrivning</div>
    <div class="description">
      Lorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit ametLorem ipsum dolor sit amet
      </div>
  </div>
</div>

<style>
  @media screen and (min-width: 850px) {
    .mainCard {
      display: flex;
    }
  }

  .mainCard {
    width: 80vw;
    background-color: white;
    padding: 3rem;
    padding-top: 0rem;
    padding-bottom:10rem;
    gap: 5rem;
  }

  .Title {
    display: flex;
    justify-content: center;
    height: 10%;
    font-size: 3rem;
    font-family: "Oswald", sans-serif;
    margin-bottom: 2rem;
    margin-top: 10vh;
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
  .description{
    padding-bottom: 1rem;
    border-bottom: 1px #EEEEEE solid;

  }

  .buy-button-container {
    display: flex;
    justify-content: center;
    align-items: center;
    border-bottom: 1px #EEEEEE solid;
    padding-bottom: 1rem;
  }

  .buy-button {
    align-items: center;
    display: flex;
    justify-content: center;
    padding: 1rem;
    width: 15rem;
    background: #1d3461;
    border-radius: 20px;
    color: #ffff;
    transition: 1000ms;
    font-family: "Oswald", sans-serif;
    font-weight: bold;
    font-size: 1.7rem;
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
