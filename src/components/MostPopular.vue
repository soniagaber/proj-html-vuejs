<script>
import PopularCard from './PopularCard.vue';
export default{
    data(){
        return{
            cards:[
                {
                    img:"/img/skin-on-fries-200x286.jpg",
                    nome:"Skin On Fries",
                    prezzo:"$3.00 - $6.00"
                },
                {
                    img:"/img/choco-cookie-frappe-200x286.jpg",
                    nome:"Choco Cookie Frappe",
                    prezzo:"$4.99"
                },
                {
                    img:"/img/donut-burger-200x286.jpg",
                    nome:"The Donut Burger",
                    prezzo:"$6.99"
                },
            ]
                
            
        }
    },
    components:{
        PopularCard
    }
}
</script>

<template>
    <div id="container-sfondo">
        <div id="container">
            <h2>Our Most Popular Dishes</h2>
            <div id="cards-container">
                <PopularCard v-for="card in cards" :obj="card"></PopularCard>
            </div>
            
            <button>start your order &nbsp;<i class="fa-solid fa-circle-arrow-right"></i></button>
        </div>
        <div id="backgr-order">
            <img id="wave" src="/img/svg-0.svg" alt="">
            <img src="/img/first-order-background-scaled.jpg" alt="">
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
    #container-sfondo{
        width:100%;
        background-color: white;
        #container{
            text-align: center;
            margin: auto;
            max-width: $container-width;
        }
        button{
            @include bottone();
            }
    }
    h2{
        text-align: center;
        color: black;
    }
    #cards-container{
        display: flex;
        justify-content: space-between;
        gap: 20px;
    }
    img{
        width: 100%;
    }
    #wave{
        position: absolute;
    }
    #backgr-order{
        position: relative;
    }
</style>