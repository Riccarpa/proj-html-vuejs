<template>
  <header>
      <div class="container">
          <div class="row justify-content-center ">
              <div class="col col-2"><button type="button" class="btn btn-danger">ORDER ONLINE</button></div>
              <div class="col col-8">
                  <ul class="main-nav h-100 d-flex align-items-center">
                      <li v-for="(item) in headerNavLeft " :key="item.index">{{item.text}}</li> 
                      <img class="img-fluid" src="../img/h5-logo-divided-header.png" alt="">  
                       <li v-for="(item) in headerNavRight " :key="item.index">{{item.text}}</li>               
                  </ul>
              </div>
              <div class="col col-2">
                  <ul class="side-nav  h-100 d-flex align-items-center">
                      <li v-for="item in headerSideNav" :key="item.index">{{item.text}}</li>
                  </ul>
              </div>
          </div>
      </div>
  </header>
</template>

<script>
export default {
name:'Header',
data(){
    return{  
        headerNavRight:[
            {
              text: 'EVENT',
              index:0 
            },
            {
                text: 'BLOG',
                index:1
            },
            {
                 text: 'LANDING',
                index:2 
            }
        ],
          headerNavLeft:[
            {
              text: 'HOME',
              index:3
            },
            {
                text: 'PAGES',
                index:4
            },
            {
                 text: 'MENU',
                index:5 
            }
        ],
        headerSideNav:[
           {
              text: 'CART',
              index:0 
            },
            {
                text: 'SEARCH',
                index:1
            },  
        ]   
    }
}
}
</script>

<style lang="scss" scoped>

@import '../scss/_style.scss';

 header{
    background-color: $head-bg;
    color: white;
    .container{
        height: 100px;
        .row{
            height: 100%;
            justify-content: center;
            align-items: center;
            .col{  
                display: flex;
                align-items: center;
                justify-content: center;
                height: 100%;
                button{
                    padding:  5 10px;
                    border-radius: 0;
                }
                img{
                    height: 80%;
                }
                ul.main-nav{
                    
                    li{
                        padding: 20px;
                        cursor: pointer;
                        &:hover{
                            transform: scale(1.1);
                        }
                        &:first-child{
                        position: relative;
                        }
                        &:first-child::before{
                        content:url('../svg/svg-0.svg');
                        position: absolute;
                        left: -10px;
                        top: 27px;
                    }
                    
                    }
                }
                ul.side-nav{

                     li{
                         margin: 20px;
                        padding: 20px;
                        cursor: pointer;
                        &:hover{
                            transform: scale(1.1);
                        }
                        position: relative;
                        &:first-child::before{
                            content:url('../svg/svg-1.svg');
                        position: absolute;
                        left: -15px;
                        top: 23px;
                        }
                        &:last-child::before{
                        content:"\26B2";
                        position: absolute;
                        left: 0;
                        top: 20px;
                        }
                       
                    }

                }

            }
        }
    }
}


</style>