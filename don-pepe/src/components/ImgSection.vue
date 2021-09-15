<template>
  <section>
      <div class="row">
          <div v-for="image in images" :key="image.id" class="img-element col-3 g-2 position-relative">
              <img class="img img-fluid " :src="image.url" alt="">
              <div class="hover-element h-100 w-100 "><i class="fas fa-glasses fa-2x"></i></div>
          </div>
       </div>
  </section>
</template>

<script>
export default {
name:'ImgSection',
data(){
    return{
        images:[
            {
                url:require('@/img/h3-img-1.jpg'),
                id:0
            },
             {
                url:require('@/img/h3-img-2.jpg'),
                id:1
            },
             {
                url:require('@/img/h3-img-3.jpg'),
                id:2
            },
             {
                url:require('@/img/h3-img-4.jpg'),
                id:3
            },
        ]
    }
}
}
</script>

<style lang="scss" scoped>

@import '../scss/_style.scss';


section{
    overflow: hidden;
}
.hover-element{
    background-image: url('../img/pattern.png');
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    display: none;
    i{
        background-color:$button-text;
        padding: 10px;
        border-radius: 50%;
    }
}
.img-element:hover .img {
    display: none;
}
.img-element:hover .hover-element{
    display: flex;
    align-items: center;
    justify-content: center;
}


</style>