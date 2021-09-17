<template>
  <section>
    <div class="menu-title text-center ">
      <span class="d-block text-uppercase">Choose your flavor</span>
      <h3 class="text-uppercase">The best pizza menu in town</h3>
      <p class="w-50">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Modi
        voluptates impedit consectetur dignissimos cum aliquam voluptatum delect
      </p>
    </div>
    <div class="pizza-menu">
      <div class="item text-center" v-for="pizza in pizzas" :key="pizza.id">
        <img :src="pizza.img" :alt="pizza.taste" />
        <h5 class="text-uppercase">{{ pizza.taste }}</h5>
        <span class="d-block">{{ pizza.price }}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Menu",
  data() {
    return {
      pizzas: [
        {
          img: require("@/img/h3-product-img-1a-100x100.png"),
          taste: "bismark",
          price: "$5.00 - $30",
          id: 0,
        },
        {
          img: require("@/img/h3-product-img-2a-150x150.png"),
          taste: "fiori di zucca",
          price: "$7.00 - $50",
          id: 1,
        },
        {
          img: require("@/img/h3-product-img-3a-150x150.png"),
          taste: "valdostana",
          price: "$55.00",
          id: 2,
        },
        {
          img: require("@/img/h3-product-img-4a-150x150.png"),
          taste: "pizza tartufata",
          price: "$45.00",
          id: 3,
        },
        {
          img: require("@/img/h3-product-img-5a-150x150.png"),
          taste: "francescana",
          price: "$25.00",
          id: 4,
        },
        {
          img: require("@/img/h3-product-img-6a-100x100.png"),
          taste: "campagnola",
          price: "$50.00 - $95.00",
          id: 5,
        },
        {
          img: require("@/img/h3-product-img-5a-150x150.png"),
          taste: "francescana",
          price: "$25.00",
          id: 6,
        },
        {
          img: require("@/img/h3-product-img-6a-100x100.png"),
          taste: "campagnola",
          price: "$50.00 - $95.00",
          id: 7,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

section {
  margin: 0.5rem 0 0.5rem 0;

  .menu-title {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 4rem;
    margin-bottom: 0;
    span {
      color: $button-text;
      font-weight: bolder;
    }
  }
  .pizza-menu {
    display: flex;
    flex-wrap: nowrap;
    overflow-x: scroll;
    .item {
      margin: 3rem;
      font-size: smaller;
      img {
        height: 200px;
        width: 200px;
      }
      h5 {
        margin-top: 1rem;
        font-size: 14px;
        color: $secondary;
      }
      span {
        color: $button-text;
        font-weight: bolder;
      }
    }
  }
}
</style>
