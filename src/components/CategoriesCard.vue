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
            <div id="nome">{{ obj.nome }}</div>
    </div>
</template>
<style lang="scss" scoped>
div{
    color: black;
    display: flex;
    flex-direction: column;
}
#card{
    width:calc(100% / 4 - 13px / 4 * 3);
    aspect-ratio: 2/1.4;
    overflow: hidden;
    position: relative;
}

#nome{
    position: absolute;
    font-size: 0.7em;
    color: white;
    font-weight: bold;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    z-index: 3;
    cursor: pointer;
}
#overlay{
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: 2;
    background-color: rgba(0, 0, 0, 0.3);
}
</style>