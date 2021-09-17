<template>
  <section>
    <div class="clients h-100">
      <img v-for="logo in logos" :key="logo.id" :src="logo.url" alt="logo" />
    </div>
  </section>
</template>

<script>
export default {
  name: "Sponsor",
  data() {
    return {
      logos: [
        {
          url: require("@/img/h1-clients-img-4.png"),
          id: 0,
        },
        {
          url: require("@/img/h1-clients-img-3.png"),
          id: 1,
        },
        {
          url: require("@/img/h1-clients-img-1.png"),
          id: 2,
        },
        {
          url: require("@/img/h1-clients-img-2.png"),
          id: 3,
        },
        {
          url: require("@/img/h1-clients-img-5.png"),
          id: 4,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  height: 200px;
  background-color: #ebebde;
  margin: 0.5rem 0 0.5rem 0;
  .clients {
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
