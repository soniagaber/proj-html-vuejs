<script>
</script>

<template>
    <div id="background-container">
        <div id="container">
            <div id="title-and-button">
                <h2>Menu Categories</h2>
                <button>view the full menu</button>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
#background-container{
    width: 100%;
    background-color: white;
    #container{
        margin: auto;
        max-width: $container-width;
        h2{
            color: black;
        }
    }
}
button{
           @include bottone();
            }
        #title-and-button{
            display: flex;
            justify-content: space-between;
            flex-direction: row;
        }
</style>