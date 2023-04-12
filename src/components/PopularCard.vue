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
    <div>
        <img :src="`${obj.img}`" alt="">
        <div id="nome">{{ obj.nome }}</div>
        <div id="prezzo">{{ obj.prezzo }}</div>
    </div>
</template>
<style lang="scss" scoped>
div{
    color: black;
    display: flex;
    flex-direction: column;
}
</style>