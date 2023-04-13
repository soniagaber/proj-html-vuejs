<script>
export default{
    data(){
        return{

        }
    },
    props:{
        obj:Object
    }
}
</script>
<template>
    <div id="card-container">
        <div id="overlay">
            <i id="cart" class="fa-regular fa-square-check"></i>
            <div id="cart-scritta">VIEW CART</div>
        </div>
        <img :src="`${obj.img}`" alt="">
        <div id="nome">{{ obj.nome }}</div>
        <div id="prezzo">{{ obj.prezzo }}</div>
    </div>
</template>
<style lang="scss" scoped>
div{
    display: flex;
    flex-direction: column;
}

#card-container{
    width:calc(100%/3 - 20px / 3 * 2);
    position: relative;
    cursor: pointer;
    &:hover #overlay{
        display: inline-block;
    }
}

#nome{
    color: #252a33;
    font-weight: bold;
    margin-top: 10px;
    margin-bottom: 3px;
}

#prezzo{
color: red;
font-size: 0.7em;
}

#overlay{
    width: 100%;
    background-color: rgba(0,0,0,0.25);
    aspect-ratio: 1/1.43;
    position: absolute;
    display: none;
}

#cart{
    padding: 9px 10.5px;
    border-radius: 50%;
    background-color: rgba(0,0,0,0.7);
    position: relative;
    top: 110px;
}

#cart-scritta{
    position: relative;
    top: 115px;
    font-weight: bold;
    font-size: 0.7em;
}

</style>