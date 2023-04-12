<script>
</script>

<template>
    <div id="background-container">
        <div id="container">
            <div id="section-text">
                <div id="download">Download Our</div>
                <div id="ordering">Ordering App</div>
                <div><img src="/img/app-store-badge-200x67.png" alt="">
                <img src="/img/play-store-badge.png" alt=""></div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
#background-container{
    width: 100%;
    position: relative;
    background-image: url('/img/app-download.jpg');
    background-size: cover;
    
    #container{
        margin: auto;
        max-width: $container-width;
        height: 100%;
    }
    }
    #section-text{
        padding: 120px 0;
        line-height: 1.9em;
    }
    #download{
    font-size: 1.3em;
    font-weight: bold;
    }
    #ordering{
    font-size: 2.5em;
    font-weight: bold;
    color: #FBDB30;
    }
    img{
        height: 28px;
        margin-top: 30px;
        margin-right: 12px;
        cursor: pointer;
    }
</style>