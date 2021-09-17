<template>
  <section>
    <div class="row h-100">
      <!-- left side -->
      <div
        class="col-6 left "
        :class="
          events
            ? 'left-ul d-flex flex-column justify-content-center bg-dark '
            : ''
        "
      >
        <!-- image -->
        <img
          v-if="combos"
          class="h-100 w-100"
          src="@/img/h1-img-4.jpg"
          alt=""
        />
        <!-- title -->
        <div v-if="events" class="title  text-white ">
          <span class="text-uppercase text-danger fw-bold "
            >Made with love</span
          >
          <h2 class="text-uppercase">delish pizza deals</h2>
        </div>
        <!-- ul -->
        <ul v-if="events" class="text-white m-4">
          <li v-for="item in datascollect" :key="item.id">
            <div class="d-flex justify-content-center ">
              <div class="price text-center">
                <span> {{ item.date }} </span>
                <span class="d-block text-white">{{ item.month }}</span>
              </div>
              <div>
                <span class="type">{{ item.event }}</span>
                <p class="text-danger">{{ item.place }}</p>
                <hr class="text-danger" />
              </div>
            </div>
          </li>
        </ul>
      </div>
      <!-- right side -->
      <div
        class="col-6 right d-flex flex-column align-items-center justify-content-center h-100 "
      >
        <div v-if="combos" class="title m-2">
          <!-- title -->
          <h2>SPECIALS*</h2>
          <p>{{ combos[0].text }}</p>
        </div>
        <!-- ul -->
        <ul v-if="combos">
          <li v-for="item in datascollect" :key="item.id">
            <div class="d-flex justify-content-center ">
              <span class="price">{{ item.price }}</span>
              <div>
                <span class="type">{{ item.size }}</span>
                <p>{{ item.text }}</p>
              </div>
            </div>
          </li>
        </ul>
        <!-- image -->
        <img v-else class="h-100 w-100" src="@/img/h3-img-5a.jpg" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HalfDividedSection",
  props: ["combos", "events"],
  computed: {
    datascollect() {
      let datas = [];
      if (this.combos) {
        datas = [...this.combos];
      }
      if (this.events) {
        datas = [...this.events];
      }

      return datas;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

section {
  height: 500px;
  margin: 0.5rem 0 0.5rem 0;
  overflow: hidden;
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
.left-ul {
  padding: 3rem;
  height: 90%;
}
</style>
