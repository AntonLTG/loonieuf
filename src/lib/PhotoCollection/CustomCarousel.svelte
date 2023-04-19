<script lang="ts">
  import darkgrey1 from "./../../assets/img/darkgrey1.png";
  import darkgrey2 from "./../../assets/img/darkgrey2.png";
  import darkgrey3 from "./../../assets/img/darkgrey3.png";
  import darkgrey4 from "./../../assets/img/darkgrey4.png";
  import darkgrey5 from "./../../assets/img/darkgrey5.png";

  import ljusgrå1 from "./../../assets/img/Ljusgrå1.png";
  import ljusgrå2 from "./../../assets/img/Ljusgrå2.png";
  import ljusgrå3 from "./../../assets/img/Ljusgrå3.png";
  import ljusgrå4 from "./../../assets/img/Ljusgrå4.png";
  import ljusgrå5 from "./../../assets/img/Ljusgrå5.png";

  import marinblue1 from "./../../assets/img/Marinblå.png";
  import marinblue2 from "./../../assets/img/Marinblå1.png";
  import marinblue3 from "./../../assets/img/Marinblå2.png";
  import marinblue4 from "./../../assets/img/Marinblå3.png";
  import marinblue5 from "./../../assets/img/Marinblå4.png";

  import bebisrosa1 from "./../../assets/img/Bebisrosa1.png";
  import bebisrosa2 from "./../../assets/img/Bebisrosa2.png";
  import bebisrosa3 from "./../../assets/img/Bebisrosa3.png";
  import bebisrosa4 from "./../../assets/img/Bebisrosa4.png";
  import bebisrosa5 from "./../../assets/img/Bebisrosa5.png";

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
      images={getImages()}
      transitionType=""
      transitionParams={{ delay: 0, duration: 0 }}
      showCaptions={false}
      showThumbs={true}
      slideControls={true}
      showIndicators={true}
      
      />
  </div>
</div>

<style>


</style>
