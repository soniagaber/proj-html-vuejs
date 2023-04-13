<!--componente che stampa tutti gli elementi del menu dell'header, passati tramite props da "AppHeader.vue"-->
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
    <!--stampa effettiva degli elementi del menu. se la classe è active, l'elemento sarà colorato di giallo-->
    <div id="links-container">
        <ul v-for="link in obj.links">
                <li :class="`${link.clas}`">
                    {{ link.scritta }}
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

.active{
    color:#FBDB30;
    &::after{content:'\f107';}
}

</style>