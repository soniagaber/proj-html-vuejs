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
        <h5 id="titolo" :class="`${obj.clas}`">{{ obj.title }}</h5>
        <ul v-for="link in obj.links" :class="`${obj.clas}`">
                <li :class="`${link.clas}`">
                    {{ link.scritta }}
                </li>
        </ul>
        <ul v-for="open in obj.opening">
                <li>
                    {{ open.giorno }} <span id="ora">{{ open.ora }}</span>
                </li>
        </ul>
        <div id="imma-lista">
            <ul v-for="imma in obj.immagini" :class="`${obj.clas}`">
                    <li>
                        <img :src="`${imma}`" alt="">
                    </li>
            </ul>
        </div>
        <ul v-for="testo in obj.testi" :class="`${obj.clas}`">
                <li>
                    {{ testo }}
                </li>
        </ul>
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

.center{text-align: center;
}

ul.center li img{border: none;
height: 100px;
width: 100px;}

.active{
    color: #FBDB30;
}
</style>