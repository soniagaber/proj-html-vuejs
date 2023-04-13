<!--sezione che contiene oggetto cards, che passa al componente figlio "LatestCard" tramite prop-->
<script>
import LatestCard from './LatestCard.vue';
export default{
    data(){
        return{
            cards:[
                {
                    img:"/img/pancake-burger-1200x900.jpg",
                    nome:"NEW: The Pancake Burger",
                    descr:"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. Pellentesque commodo tortor vel mi"
                },
                {
                    img:"/img/new-milkshake-menu-200x150.jpg",
                    nome:"New Milkshake Menu",
                    descr:"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. Pellentesque commodo tortor vel mi"
                }
            ]
                
            
        }
    },
    components:{
        LatestCard
    }
}
</script>

<template>
    <div id="background-container">
        <div id="container">
            <div id="title-and-button">
                <h2>Latest News</h2>
                <button>read more news &nbsp;<i class="fa-solid fa-circle-arrow-right"></i></button>
            </div>
            <div id="cards-container">
                <LatestCard v-for="card in cards" :obj="card"></LatestCard>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
h2{
    @include titoloSection();
}
#background-container{
    padding-top: 85px;
    background-color: white;
    padding-bottom: 110px;
    #container{
        margin: auto;
        max-width: $container-width;
    }
}
button{
           @include bottone();
            }
        #title-and-button{
            display: flex;
            justify-content: space-between;
            flex-direction: row;
            align-items: center;
        }
#cards-container{
        display: flex;
        justify-content: space-between;
        gap: 25px;
        margin-top: 30px;
    }
</style>