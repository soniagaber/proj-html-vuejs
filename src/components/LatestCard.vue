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
    <div id="card">
        <div id="overlay"></div>
        <img :src="`${obj.img}`" alt="">
        <h3 id="nome">{{ obj.nome }}</h3>
        <div id="descr">{{ obj.descr }}</div>
    </div>
</template>
<style lang="scss" scoped>
div{
    color: black;
    display: flex;
    flex-direction: column;
}
#card{
    width:calc(100% / 2 - 25px / 2);
    text-align: center;
    position: relative;
    cursor: pointer;
    &:hover #overlay{
        display: block;
    }
    #overlay{
        aspect-ratio: 2/1.5;
        width: 100%;
        background-color: rgba(0, 0, 0, 0.25);
        position: absolute;
        z-index: 2;
        display: none;
    }
}
h3{
    margin-top: 25px;
    color: #252a33;
    font-size: 1.5em;
}
#descr{
    color: #323844;
    font-size: 0.68em;
}
</style>