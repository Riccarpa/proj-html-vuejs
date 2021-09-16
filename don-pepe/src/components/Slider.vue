<template>
  <section>
    <div
      id="carouselExampleControls"
      class="carousel slide "
      :class="citazioni ? 'bg2 mt-2' : 'bg1'"
      data-bs-ride="carousel"
    >
      <div class="h-100 position-relative">
        <div class="carousel-inner h-100">
          <!-- slider 1 images -->
          <div
            v-for="img in images"
            :key="img.id"
            class="carousel-item "
            :class="img.id == 0 ? 'active' : ''"
          >
            <div class="img-center position-relative">
              <img class="bg" :src="img.bgUrl" alt="" />
              <img :src="img.url" class="d-block " alt="..." />
            </div>
          </div>
          <!-- slider 2  citazioni -->
          <div
            v-for="item in citazioni"
            :key="item.id"
            class="carousel-item "
            :class="item.id == 0 ? 'active' : ''"
          >
            <div class="img-center position-relative">
              <img class="bg" :src="item.bgUrl" alt="" />
              <div class="cit">
                <i
                  class="fas fa-quote-right d-block mb-4 fa-2x text-danger"
                ></i>
                <span class="text">{{ item.text }}</span>
                <span class="text-danger d-block m-2"
                  >WASHINGTON POST 2018
                </span>
                <i class="fas fa-ellipsis-h fa-2x text-danger"></i>
              </div>
            </div>
          </div>
        </div>
        <!-- buttons -->
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleControls"
          data-bs-slide="prev"
        >
          <div class="carousel-control-prev" aria-hidden="true">
            <span class="prev button">PREV</span>
          </div>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleControls"
          data-bs-slide="next"
        >
          <div class="carousel-control-next" aria-hidden="true">
            <span class="next button">NEXT</span>
          </div>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Slider",
  props: ["images", "citazioni"],
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

// slider images
.bg1 {
  background-color: $head-bg;
  height: 400px;
}
// generics
section {
  overflow: hidden;
}
.carousel-item {
  height: 100%;

  .img-center {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      height: 300px;
      z-index: 1;
    }
    .bg {
      position: absolute;
      z-index: 0;
    }
  }
}
.carousel-control-next,
.carousel-control-prev {
  opacity: 1;
  .button {
    position: absolute;
    background-color: white;
    padding: 10px 10px 20px 10px;
    color: $button-text;
    border-radius: 50%;
    border-radius: 50%;
  }
  .next {
    transform: rotate(270deg);
    right: -50%;
    top: 35%;
  }
  .prev {
    transform: rotate(90deg);
    left: -50%;
    top: 35%;
  }
}
// slider citazioni
.bg2 {
  background-color: #f6f7f2;
  height: 300px;
  .cit {
    z-index: 1;
    text-transform: uppercase;
    width: 600px;
    text-align: center;
    .text {
      font-weight: 600;
      font-size: 20px;
    }
  }
}
</style>
