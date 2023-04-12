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
            
            <button>start your order</button>
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
            background-color: #CD1925;
            margin-top: 16px;
            border-radius: 25px;
            padding: 7px 12px;
            color: white;
            border: none;
            font-size: 0.5em;
            font-weight: bold;
            text-transform: uppercase;
            cursor:pointer;
            }
    }
    h2{
        text-align: center;
        color: black;
    }
    #cards-container{
        display: flex;
        justify-content: space-between;
    }
</style>