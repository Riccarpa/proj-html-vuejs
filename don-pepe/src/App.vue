<template>
  <div id="app">
    <Header />
    <main>
      <Slider :images="tasteSliderImg" />
      <ImgSection :images1="imgSection1" />
      <Slider :citazioni="testimonialSlider" />
      <HalfDividedSection :combos="pizzaSpecials" />
      <YourOwnPizza />
      <ImgSection :images2="imgSection2" />
      <Sponsor />
      <Menu />
      <HalfDividedSection :events="events" />
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Slider from "@/components/Slider.vue";
import ImgSection from "@/components/ImgSection.vue";
import HalfDividedSection from "@/components/HalfDividedSection.vue";
import YourOwnPizza from "@/components/YourOwnPizza.vue";
import Sponsor from "@/components/Sponsor.vue";
import Menu from "@/components/Menu.vue";

export default {
  name: "App",
  components: {
    Header,
    Slider,
    ImgSection,
    HalfDividedSection,
    YourOwnPizza,
    Sponsor,
    Menu,
  },
  data() {
    return {
      tasteSliderImg: [
        {
          url: require("@/img/h3-rev-img-2.png"),
          bgUrl: require("@/img/h3-rev-img-1.png"),
          id: 0,
        },
        {
          url: require("@/img/h3-rev-img-4.png"),
          bgUrl: require("@/img/h3-rev-img-3.png"),
          id: 1,
        },
        {
          url: require("@/img/h3-rev-img-6.png"),
          bgUrl: require("@/img/h3-rev-img-5.png"),
          id: 2,
        },
      ],
      testimonialSlider: [
        {
          text:
            "forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in naples",
          bgUrl: require("@/img/h3-testimonials-bckgrnd.jpg"),
          id: 0,
        },
        {
          text:
            "forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in naples",
          bgUrl: require("@/img/h3-testimonials-bckgrnd.jpg"),
          id: 1,
        },
        {
          text:
            "forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in naples",
          bgUrl: require("@/img/h3-testimonials-bckgrnd.jpg"),
          id: 2,
        },
      ],
      imgSection1: [
        {
          url: require("@/img/h3-img-1.jpg"),
          id: 0,
        },
        {
          url: require("@/img/h3-img-2.jpg"),
          id: 1,
        },
        {
          url: require("@/img/h3-img-3.jpg"),
          id: 2,
        },
        {
          url: require("@/img/h3-img-4.jpg"),
          id: 3,
        },
      ],
      pizzaSpecials: [
        {
          size: "combo piccolo",
          text:
            "lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent dui",
          price: "$10",
          id: 0,
        },
        {
          size: "combo medio",
          text:
            "lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent dui",
          price: "$20",
          id: 1,
        },
        {
          size: "combo grande",
          text:
            "lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent dui",
          price: "$30",
          id: 2,
        },
      ],
      imgSection2: [
        {
          url: require("@/img/h1-team-1a-700x700.jpg"),
          name: "Marco Rossi",
          role: "Cameriere",
          id: 0,
        },
        {
          url: require("@/img/h1-team-2a.jpg"),
          name: "Lucia Rossi",
          role: "Pizzaiola",
          id: 1,
        },
        {
          url: require("@/img/h1-team-3a.jpg"),
          name: "paola Rossi",
          role: "Lavapiatti",
          id: 2,
        },
        {
          url: require("@/img/h1-team-4a.jpg"),
          name: "Giacomo Rossi",
          role: "Direttore di sala",
          id: 3,
        },
      ],
      events: [
        {
          event: "traditional neapolitan pies in kioto pizza mercato",
          place: "204E. Pizzetta Tommaso",
          date: "02",
          month: "NOV",
          id: 0,
        },
        {
          event: "terrazza patio dining space opening this weekend",
          place: "204E. Pizzetta Tommaso",
          date: "03",
          month: "NOV",
          id: 1,
        },
        {
          event: "sienna private dining room with stephane brunn",
          place: "204E. Pizzetta Tommaso",
          date: "05",
          month: "NOV",
          id: 2,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "bootstrap";
@import "./scss/_style.scss";
</style>
