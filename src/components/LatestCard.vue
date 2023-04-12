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
}
h3{
    color: #252a33;
}
#descr{
    color: #323844;
    font-size: 0.68em;
}
</style>