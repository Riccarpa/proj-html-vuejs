<template>
  <section>
    <div class="row h-100">
      <!-- left side -->
      <div class="col-6 left h-100">
        <img class="h-100 w-100" src="@/img/h1-img-4.jpg" alt="" />
      </div>
      <!-- right side -->
      <div
        class="col-6 right d-flex flex-column align-items-center justify-content-center  "
      >
        <div class="title m-2">
          <!-- title -->
          <h2>SPECIALS*</h2>
          <p>{{ combos[0].text }}</p>
        </div>
        <ul>
          <!-- ul -->
          <li v-for="item in combos" :key="item.id">
            <div class="d-flex justify-content-center ">
              <span class="price">{{ item.price }}</span>
              <div>
                <span class="type">{{ item.size }}</span>
                <p>{{ item.text }}</p>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HalfDividedSection",
  props: ["combos"],
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

section {
  height: 500px;
  margin: 0.5rem 0 0.5rem 0;
  overflow-x: hidden;
}
p {
  width: 80%;
}
.type {
  text-transform: uppercase;
  font-weight: bold;
}
.price {
  color: $button-text;
  margin: 0 1rem 0 2.5rem;
  font-weight: bold;
}
</style>
