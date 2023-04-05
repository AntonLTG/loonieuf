<script lang="ts">
  import darkgrey1 from "./../../assets/img/darkgrey1.jpg";
  import darkgrey2 from "./../../assets/img/darkgrey2.jpg";
  import darkgrey3 from "./../../assets/img/darkgrey3.jpg";
  import darkgrey4 from "./../../assets/img/darkgrey4.jpg";
  import darkgrey5 from "./../../assets/img/darkgrey5.jpg";

  import ljusgrå1 from "./../../assets/img/Ljusgrå1.jpg";
  import ljusgrå2 from "./../../assets/img/Ljusgrå2.jpg";
  import ljusgrå3 from "./../../assets/img/Ljusgrå3.jpg";
  import ljusgrå4 from "./../../assets/img/Ljusgrå4.jpg";
  import ljusgrå5 from "./../../assets/img/Ljusgrå5.jpg";

  import marinblue1 from "./../../assets/img/Marinblå.jpg";
  import marinblue2 from "./../../assets/img/Marinblå1.jpg";
  import marinblue3 from "./../../assets/img/Marinblå2.jpg";
  import marinblue4 from "./../../assets/img/Marinblå3.jpg";
  import marinblue5 from "./../../assets/img/Marinblå4.jpg";

  import bebisrosa1 from "./../../assets/img/Bebisrosa1.jpg";
  import bebisrosa2 from "./../../assets/img/Bebisrosa2.jpg";
  import bebisrosa3 from "./../../assets/img/Bebisrosa3.jpg";
  import bebisrosa4 from "./../../assets/img/Bebisrosa4.jpg";
  import bebisrosa5 from "./../../assets/img/Bebisrosa5.jpg";

  import { CarouselTransition } from "flowbite-svelte";
  import type { ColorTypes } from "./types";

  export let picColor: ColorTypes;

  const marinblåImages = [
    {
      id: 0,
      name: "Cosmic timetraveler",
      imgurl: marinblue1,
    },
    {
      id: 1,
      name: "Cosmic timetraveler",
      imgurl: marinblue2,
    },
    {
      id: 2,
      name: "Cosmic timetraveler",
      imgurl: marinblue3,
    },
    {
      id: 3,
      name: "Cosmic timetraveler",
      imgurl: marinblue4,
    },
    {
      id: 4,
      name: "Cosmic timetraveler",
      imgurl: marinblue5,
    },
  ];

  const bebisrosaImages = [
    {
      id: 0,
      name: "Cosmic timetraveler",
      imgurl: bebisrosa1,
    },
    {
      id: 1,
      name: "Cosmic timetraveler",
      imgurl: bebisrosa2,
    },
    {
      id: 2,
      name: "Cosmic timetraveler",
      imgurl: bebisrosa3,
    },
    {
      id: 3,
      name: "Cosmic timetraveler",
      imgurl: bebisrosa4,
    },
    {
      id: 4,
      name: "Cosmic timetraveler",
      imgurl: bebisrosa5,
    },
  ];

  const ljusgråImages = [
    {
      id: 0,
      name: "Cosmic timetraveler",
      imgurl: ljusgrå1,
    },
    {
      id: 1,
      name: "Cosmic timetraveler",
      imgurl: ljusgrå2,
    },
    {
      id: 2,
      name: "Cosmic timetraveler",
      imgurl: ljusgrå3,
    },
    {
      id: 3,
      name: "Cosmic timetraveler",
      imgurl: ljusgrå4,
    },
    {
      id: 4,
      name: "Cosmic timetraveler",
      imgurl: ljusgrå5,
    },
  ];

  const darkgreyImages = [
    {
      id: 0,
      name: "Cosmic timetraveler",
      imgurl: darkgrey1,
    },
    {
      id: 1,
      name: "Cosmic timetraveler",
      imgurl: darkgrey2,
    },
    {
      id: 2,
      name: "Cosmic timetraveler",
      imgurl: darkgrey3,
    },
    {
      id: 3,
      name: "Cosmic timetraveler",
      imgurl: darkgrey4,
    },
    {
      id: 4,
      name: "Cosmic timetraveler",
      imgurl: darkgrey5,
    },
  ];

  $: getImages = () => {
    if (picColor == "Mörkgrå") {
      return darkgreyImages;
    }
    if (picColor == "Ljusgrå") {
      return ljusgråImages;
    }
    if (picColor == "Bebis rosa") {
      return bebisrosaImages;
    }
    if (picColor == "Marin blå") {
      return marinblåImages;
    }
    return [];
  };
</script>

<div class="wrapper">
  <div class="container">
    <CarouselTransition
      divClass="asd"
      images={getImages()}
      transitionType="fly"
      transitionParams={{ delay: 250, duration: 300 }}
      showCaptions={false}
      showThumbs={true}
    />
  </div>
</div>

<style>
  .wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .container {
    width: 50%;
  }
  .asd img {
    height: 100px;
  }
</style>
