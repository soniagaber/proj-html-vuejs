<script>
import HeaderMenuItem from './HeaderMenuItem.vue';

export default{
    data(){
        return{
            items:[
                {
                    links:[
                    {scritta:'Home ',
                    clas:"active"},
                    {scritta:'Order Online'},
                    {scritta:'About'},
                    {scritta:'News'},
                    {scritta:'Contact Us'},
                    ],
                    icons:['fa-solid fa-cart-shopping']
                }
            ],
        }
    },
    components:{
        HeaderMenuItem,
    }
}
</script>

<template>
    <div id="container-sfondo">
        <div class="fixed">
        +
        </div>
        <div id="container">
            <nav>
                <img src="/img/takeout-logo-mobile.png" alt="">
                <div>
                <HeaderMenuItem v-for="item in items" :obj="item"></HeaderMenuItem>
                </div>
            </nav>
            <div id="header-text">
                <div id="hungry">Hungry?</div>
                <div id="great">Great Food</div>
                <div id="deliv">Delivered</div>
                <button>view our menu &nbsp;<i class="fa-solid fa-circle-arrow-right"></i></button>
            </div>
    </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
#container-sfondo{
    height: 590px;
    background-image: url('/img/home-background-hero-scaled.jpg');
    background-position-y: -120px;
    background-size: cover;
    width: 100%;
    position: relative;
}

#container{
    max-width: $container-width;
    margin: auto;
}

nav{
    display: flex;
    justify-content: space-between;
    padding-top: 40px;
    align-items: center;
}

#header-text{
   position: absolute;
   top: 50%;
   transform: translateY(-50%);
   gap: 0px;
   line-height: 2.45em;
   #hungry{
    font-size: 1.3em;
    font-weight: bold;
   }
   #great{
    font-size: 2.5em;
    font-weight: bold;
    color: #FBDB30;
   }
   #deliv{
    font-size: 2.5em;
    font-weight: bold;
   }
   button{
    @include bottone();
   }
    
}

img{height: 34px;}
div.fixed {
  position: fixed;
  top: 7px;
  right: 15px;
  width: 35px;
  height: 35px;
  background-color: #CD1925;
  z-index: 3;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  &:hover{
    background-color: #AA131D;
  }
}
</style>