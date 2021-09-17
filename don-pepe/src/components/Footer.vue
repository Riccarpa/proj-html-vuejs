<template>
  <footer>
    <div class="row h-100">
      <div class="footer-left col-7">
        <div class="inner-footer">
          <div class="restaurants ">
            <h5 class="text-uppercase yellow ">find our restaurants</h5>
            <ul>
              <li v-for="item in restaurants" :key="item.id">
                <span class="d-block">{{ item.indirizzo }}</span>
                <span class="d-block">{{ item.provincia }}</span>
                <span class="d-block">{{ item.contatto }}</span>
              </li>
            </ul>
          </div>
          <div class="working-hours">
            <h5 class="text-uppercase yellow ">working hours</h5>
            <ul>
              <li v-for="item in hours" :key="item.id">
                <h6 class="text-uppercase yellow">{{ item.day }}</h6>
                <span class="d-block">{{ item.info }}</span>
              </li>
            </ul>
            <div class="social text-white mt-5">
              <span class="yellow text-uppercase">follow us:</span>
              <i class="fab fa-instagram me-2 ms-2"></i>
              <i class="fab fa-facebook me-2"></i>
              <i class="fab fa-twitter me-2"></i>
              <i class="fab fa-linkedin me-2"></i>
            </div>
          </div>
        </div>
        <div class="developer">
          <span class="yellow"
            >Created with &hearts; by <a href="#">Riccardo</a>
          </span>
        </div>
        <span class="slogan text-uppercase  text-white"
          >The don peppe crew first and foremost values an authentic, well baked
          slice of pizza.</span
        >
        <img class="quality-logo " src="@/img/quality-logo.jpg" alt="" />
      </div>
      <div class="image col-5 h-100"></div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      restaurants: [
        {
          indirizzo: "1614 E. Bell rd #104.",
          provincia: "Salerno,AZ 85022",
          contatto: "(602)867-1010",
          id: 0,
        },
        {
          indirizzo: "1614 E. Bell rd #104.",
          provincia: "Salerno,AZ 85022",
          contatto: "(602)867-1010",
          id: 1,
        },
        {
          indirizzo: "1614 E. Bell rd #104.",
          provincia: "Salerno,AZ 85022",
          contatto: "(602)867-1010",
          id: 2,
        },
        {
          indirizzo: "1614 E. Bell rd #104.",
          provincia: "Salerno,AZ 85022",
          contatto: "(602)867-1010",
          id: 3,
        },
      ],
      hours: [
        {
          day: "monday",
          info: "kitchen closed",
          id: 0,
        },
        {
          day: "Tuesday until friday",
          info: "9:00 - 22:00",
          id: 1,
        },
        {
          day: "Saturday",
          info: "11:00 - 24:00",
          id: 2,
        },
        {
          day: "sunday",
          info: "9:00 - 22:00",
          id: 3,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/_style.scss";

footer {
  background-color: $head-bg;
  height: 500px;
  overflow-x: hidden;
  .image {
    background-image: url("../img/footer-img-1.jpg");
    background-size: cover;
    background-position: 30%;
  }
  .footer-left {
    position: relative;
    .inner-footer {
      display: flex;
      margin: 4rem 0 0 2rem;
      height: 300px;
    }
    .restaurants {
      margin-right: 5rem;
      font-size: 12px;
    }
    .working-hours {
      font-size: 12px;
    }
    .slogan {
      width: 200px;
      position: absolute;
      top: 12%;
      right: 5%;
    }
    .quality-logo {
      width: 100px;
      height: 100px;
      position: absolute;
      right: 5%;
      bottom: 5%;
    }
    .developer {
      position: absolute;
      bottom: 5%;
      left: 5%;
      a {
        text-decoration: none;
        color: green;
      }
    }
    li {
      margin: 1rem 0 0 0;
      span {
        color: gray;
      }
    }
  }
}

.yellow {
  color: #b7903c;
}
</style>
