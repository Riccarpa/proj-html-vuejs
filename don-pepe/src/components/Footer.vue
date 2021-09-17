<template>
  <footer>
    <div class="row h-100">
      <div class="col-6"></div>
      <div class="image col-6 h-100"></div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

footer {
  background-color: $head-bg;
  height: 500px;
  .image {
    background-image: url("../img/footer-img-1.jpg");
    background-size: cover;
    background-position: 30%;
  }
}
</style>
