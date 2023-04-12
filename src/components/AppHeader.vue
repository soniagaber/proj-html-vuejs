<script>
import HeaderMenuItem from './HeaderMenuItem.vue';

export default{
    data(){
        return{
            menu:['Home',
            'Order Online',
            'About',
            'News',
            'Contact Us']
        }
    },
    components:{
        HeaderMenuItem,
    }
}
</script>

<template>
    <div id="container-sfondo">
        <div id="container">
            <nav>
                <img src="/img/takeout-logo-mobile.png" alt="">
                <ul>
                <HeaderMenuItem v-for="men in menu" :text="men"></HeaderMenuItem>
                </ul>
            </nav>
            <div id="header-text">
                <div id="hungry">Hungry?</div>
                <div id="great">Great Food</div>
                <div id="deliv">Delivered</div>
                <button>view our menu</button>
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
    ul{
        display: flex;
        flex-direction: row;
        list-style-type: none;
        gap: 15px;
    }
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
    background-color: #CD1925;
    margin-top: 16px;
    border-radius: 25px;
    padding: 7px 12px;
    color: white;
    border: none;
    font-size: 0.5em;
    font-weight: bold;
    text-transform: uppercase;
    cursor:pointer
   }
    
}

img{height: 34px;}
</style>