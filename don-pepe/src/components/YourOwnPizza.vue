<template>
  <section>
    <div class="position-relative">
      <h1>go ahead and build your own pizza we won't judge</h1>
      <div class="row top">
        <div class="col-1">></div>
        <div class="col-10">></div>
        <div class="col-1">></div>
      </div>
      <div class="row mid">
        <div class="col-1">></div>
        <div class="col-10">></div>
        <div class="col-1">></div>
      </div>
      <div class="row bott">
        <div class="col-1">></div>
        <div class="col-10">></div>
        <div class="col-1">></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "YourOwnPizza",
};
</script>

<style lang="scss" scoped>
.row {
  padding: 0;
  margin: 0;

  &.top,
  &.bott {
    height: 100px;
  }
  &.mid {
    height: 200px;
  }
  .col-1,
  .col-10 {
    height: 100%;
    padding: 0;
    margin: 0;
    background-image: url("../img/h3-background-img.jpg");
  }
}
.top .col-1,
.top .col-10 {
  background-position: 70% 90%;
}
.bott .col-1,
.bott .col-10 {
  background-position: 80% 40%;
}
.mid .col-1,
.mid .col-10 {
  background-position: 50% 15%;
}

h1 {
  position: absolute;
  top: 50%;
  left: 30%;
  transform: translate(-50%, -50%);
  width: 250px;
  color: white;
  text-transform: uppercase;
}
</style>
