<script>
export default{
    data(){
        return{

        }
    },
    props:{
        text:String,
    }
}
</script>
<template>
    <li>
        {{ text }}
    </li>
    
</template>
<style scoped lang="scss">

li{
 font-weight: bold;
 font-size: 0.8em;
 cursor: pointer;
 &:hover{
    color:  #FBDB30;
 }
}

</style>