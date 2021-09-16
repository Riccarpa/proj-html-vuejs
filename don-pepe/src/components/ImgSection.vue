<template>
  <section>
    <div class="row">
      <div
        v-for="item in dataCollect"
        :key="item.id"
        class="img-element col-3  position-relative"
        :class="images1 ? 'g-2' : 'g-0 mt-2'"
      >
        <img class="img img-fluid " :src="item.url" alt="" />
        <div class="hover-element h-100 w-100 ">
          <i v-if="images1" class="fas fa-glasses fa-2x"></i>
          <div class="people-hover" v-else>
            <div class="text-center text-light">
              <h3 class="text-uppercase">{{ item.name }}</h3>
              <p class="text-capitalize">{{ item.role }}</p>
              <i class="fab fa-instagram"></i>
              <i class="fab fa-twitter"></i>
              <i class="fab fa-facebook"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ImgSection",
  props: ["images1", "images2"],
  computed: {
    dataCollect() {
      let datas = [];
      if (this.images1) {
        datas = [...this.images1];
      }
      if (this.images2) {
        datas = [...this.images2];
      }

      return datas;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

section {
  overflow: hidden;
}
.hover-element {
  background-image: url("../img/pattern.png");
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: none;
  i {
    background-color: $button-text;
    padding: 10px;
    border-radius: 50%;
  }
}
.img-element:hover .img {
  display: none;
}
.img-element:hover .hover-element {
  display: flex;
  align-items: center;
  justify-content: center;
}

.people-hover {
  width: 90%;
  height: 90%;
  background-color: $button-text;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
