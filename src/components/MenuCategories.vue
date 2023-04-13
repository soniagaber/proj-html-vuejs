<!--sezione che contiene oggetto cards e lo passa al figlio "CategoriesCard" tramite prop-->
<script>
import CategoriesCard from './CategoriesCard.vue';
export default{
    data(){
        return{
            cards:[
                {
                    img:"/img/appetizers-menu-background.jpg",
                    nome:"APPETIZERS",
                },
                {
                    img:"/img/burgers-menu-background.jpg",
                    nome:"BURGERS",
                },
                {
                    img:"/img/pizza-menu-background.jpg",
                    nome:"PIZZAS",
                },
                {
                    img:"/img/fries-menu-background.jpg",
                    nome:"FRIES",
                },
                {
                    img:"/img/sides-menu-background.jpg",
                    nome:"SIDES",
                },
                {
                    img:"/img/desserts-menu-background.jpg",
                    nome:"DESSERTS",
                },
                {
                    img:"/img/beverages-menu-background.jpg",
                    nome:"BEVERAGES",
                },
                {
                    img:"/img/specials-menu-background.jpg",
                    nome:"SPECIALS",
                }
            ]
                
            
        }
    },
    components:{
        CategoriesCard
    }
}
</script>

<template>
    <div id="background-container">
        <div id="container">
            <div id="title-and-button">
                <h2>Menu Categories</h2>
                <button>view the full menu &nbsp;<i class="fa-solid fa-circle-arrow-right"></i></button>
            </div>
            <div id="cards-container">
                <CategoriesCard v-for="card in cards" :obj="card"></CategoriesCard>
            </div>
            <div id="icons">
                <i class="fa-solid fa-leaf"></i> 
                <i class="fa-solid fa-wheat-awn"></i>
                <i class="fa-sharp fa-solid fa-cow"></i>
                <i class="fa-solid fa-drumstick-bite"></i>
            </div>
            <div id="icons-text">
                <div> Vegetarian</div>
                <div> Gluten Free</div>
                <div> Dairy Free</div>
                <div> Keto Friendly</div>
            </div>
            
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
#background-container{
    width: 100%;
    background-color: white;
    padding-top: 75px;
    #container{
        margin: auto;
        max-width: $container-width;
        h2{
            @include titoloSection();
        }
    }
}
button{
           @include bottone();

            }
        #title-and-button{
            display: flex;
            justify-content: space-between;
            flex-direction: row;
        }
        #cards-container{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        gap: 13px;
        margin-top: 28px;
    }
    i{
        color:red
    }
    button i{color:white}
    #icons i:first-of-type{
        color: green;
    }
    #icons i:nth-of-type(2){
        color:#E7B928;
    }
    #icons i:nth-of-type(3){
        color:#0495ce;
    }
    #icons i:nth-of-type(4){
        color:#654321;
    }

    #icons{
        font-size: 2.3em;
        display: flex;
        justify-content: space-around;
        margin-top: 47px;
    }
    #icons-text{
        color: black;
        display: flex;
        justify-content: space-around;
        gap: 80px;
        font-weight: bold;
        padding-bottom: 85px;
        font-size: 0.85em;
    }

</style>