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
    <div id="column">
        <h5 id="titolo">{{ obj.title }}</h5>
        <ul v-for="link in obj.links">
                <li>
                    {{ link }}
                </li>
        </ul>
        <ul v-for="open in obj.opening">
                <li>
                    {{ open.giorno }} <span id="ora">{{ open.ora }}</span>
                </li>
        </ul>
        <div id="imma-lista">
            <ul v-for="imma in obj.immagini">
                    <li>
                        <img :src="`${imma}`" alt="">
                    </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
div{
    color: black;
    display: flex;
    flex-direction: column;
}
#column{
    width:calc(100% / 5 - 110px / 5 * 4);
}
h5{
    color: white;
    font-size: 0.58em;
    line-height: 3.4em;
}
li{
    color: white;
    font-size: 0.5em;
    cursor: pointer;
    line-height: 2.35em;
    font-weight: bold;
    &:hover{color:#FBDB30;}
}
img{
    width:85px;
    border: 1px solid white;
    border-radius: 4px;
}
#imma-lista{
    padding-top: 10px;
}
#ora{
    color: #FBDB30;
}
</style>