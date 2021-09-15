<template>
  <section>
    <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
        <div class="h-100 position-relative">
            <div class="carousel-inner h-100">
                <div v-for="img in images" :key="img.id"  class="carousel-item " :class="img.id==0 ? 'active' : ''">
                    <div class="img-center position-relative">
                        <img class="bg" :src="img.bgUrl" alt="">
                        <img :src="img.url" class="d-block " alt="...">
                    </div>
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
                <div class="carousel-control-prev" aria-hidden="true"><span class="prev button">PREV</span></div>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
                <div class="carousel-control-next" aria-hidden="true"><span class="next button">NEXT</span></div>
                <span class="visually-hidden">Next</span>
            </button>
        </div>
       
     </div> 
     
  </section>
</template>

<script>

export default {
name:'Slider',
props:['images'],

}


</script>

<style lang="scss" scoped>

    @import '../scss/_style.scss';
    section{
        overflow: hidden;
    }
    .carousel{
        height: 400px;
        background-color: $head-bg;   
    }
    .carousel-item{
        height: 100%;
        
        
        .img-center{
            height: 100%;
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
           img{
               height: 300px;
               z-index: 1;
           }
           .bg{
               position: absolute;
               z-index: 0;
           }
        }
    }
    .carousel-control-next, 
    .carousel-control-prev{
        opacity: 1;
        .button{
           position: absolute;
           background-color: white;
           padding: 10px 10px 20px 10px;
           color: $button-text;
           border-radius: 50%;
           border-radius: 50%;
        }
        .next{
          transform: rotate(270deg);
          right: -50%;
          top: 35%;
        }
        .prev{
          transform: rotate(90deg);
          left: -50%;
          top: 35%;
        }
    }
    
</style>