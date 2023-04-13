<!--seconda sezione, passa al componente figlio, "PopularCard", oggetto i cui elementi sono da stampare, tramite props-->
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
            <div id="barra">
                <div><i class="fa-regular fa-clock"></i> &nbsp; 24/7 DELIVERY</div>
                <div><i class="fa-solid fa-burger"></i>  &nbsp; OVER 100 DISHES</div>
                <div><i class="fa-solid fa-mobile-screen-button"></i>  &nbsp; IN APP ORDERING</div>
                <div><i class="fa-solid fa-car"></i> &nbsp; FAST DELIVERY</div>
            </div>
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
        padding-top: 70px;
        #container{
            text-align: center;
            margin: auto;
            max-width: $container-width;
            position: relative;
        }
        button{
            @include bottone();
            }
    }
    h2{
        text-align: center;
        color: black;
        font-size: 1.8em;
    }
    #cards-container{
        display: flex;
        justify-content: space-between;
        gap: 20px;
        padding-top: 40px;
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
    #barra{
        color: #252a33;
        font-weight: bold;
        font-size: 0.65em;
        width: 100%;
        display: flex;
        justify-content: space-around;
        position: absolute;
        top: -96px;
        background-color: white;
        padding-top: 30px;
    }
</style>