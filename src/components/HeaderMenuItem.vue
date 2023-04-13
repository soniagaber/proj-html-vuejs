<script>
export default{
    data(){
        return{

        }
    },
    props:{
        obj:Object,
    }
}
</script>
<template>
    <div id="links-container">
        <ul v-for="link in obj.links">
                <li>
                    {{ link }}
                </li>
        </ul>
        <ul v-for="icon in obj.icons">
                    <li>
                        <i :class="`${icon}`"></i>
                    </li>
        </ul>
    </div>
    
</template>
<style scoped lang="scss">

#links-container{
        display: flex;
        flex-direction: row;
        gap: 27px;
    }

li{
 font-weight: bold;
 font-size: 0.8em;
 cursor: pointer;
 &:hover{
    color:  #FBDB30;
 }
}

</style>