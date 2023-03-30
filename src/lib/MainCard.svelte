<script lang="ts">
  import { Router, Link, Route } from "svelte-navigator";
  import blankethoodiegirl from "./../assets/img/blankethoodie.png";
  import Logo from "./../assets/img/Logo-loonieshop.png";

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
    <div class="Title">Loonie Hoodie</div>
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
    <div class="description-title">Beskrivning</div>
    <div class="description">
      Denna unika hoodie är inte bara en vanlig tröja, det är också en filt
      gjord av det mjukaste och mest isolerande materialet. Den kommer hålla dig
      varm och skön hela säsongen. Men det är inte allt - den har en huva och
      gosiga fickor så du kan krypa ihop och hålla händerna varma också. Perfekt
      för lata dagar hemma, lägereldar, camping och mer. Vår Blanket Hoodie är
      det perfekta valet för dig som söker ett extra tillskott av mys i
      vardagen. Oavsett om du vill ta det lugnt med en bra bok, titta på en film
      eller bara behöver ett extra lager på en kall dag, kommer vår hoodie ge
      dig ultimat komfort och värme. Dessutom kommer du se snygg ut medan du
      känner dig skön. Så varför vänta? Beställ din Big Cozy Blanket Hoodie idag
      och upplev skillnaden själv. Varför nöja dig med att bara vara varm när du
      kan vara varm, mysig och snygg på samma gång? Beställ nu och kryp in i det
      ultimata myskapet!"
    </div>
    <div class="pris">Pris: 400 Kr</div>
    <div class="storlek">Storlek: One Size</div>
    <div>Oversized design</div>
    <div class="storlek">Välj Antal</div>
    <div class="buy-button-container">
      <Link to="/checkout">
      <div class="buy-button">Köp</div>
      </Link>
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
    gap: 5rem;
  }

  .Title {
    display: flex;
    justify-content: center;
    height: 10%;
    font-size: 3rem;
    font-family: "Oswald", sans-serif;
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
    margin-top: 10vh;
  }



  .buy-button-container {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .buy-button {
    align-items: center;
    display: flex;
    justify-content: center;
    padding: 2rem;
    width: 15rem;
    background: #1d3461;
    border-radius: 20px;
    color: #ffff;
    transition: 1000ms;
    font-family: "Oswald", sans-serif;
    font-weight: bold;
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
