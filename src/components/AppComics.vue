<script>
import ComicItem from "./ComicItem.vue"

// importo il file dc-comics.json
import comicsFile from '../data/dc-comics.json';

export default {
    name: 'AppComics',

    components:  {
        ComicItem,
    },

    data() {
        return {

            comicsFile,

         

        }
    }

}

</script>

<template>

<div id="comics">

    <div class="container">

        <h2>
            Current Series
        </h2>
    
        <div id="comics-list">
            
            <ComicItem 
                v-for="comic in comicsFile"
                :comic="comic"
            ></ComicItem>

        </div>

        <div class="btn-container">
            <button class="btn btn-primary">Load more</button>
        </div>
    </div>

</div>

</template>

<style lang="scss">
@use '../styles/variables' as *;

#comics-list {
    display: flex;
    flex-flow: wrap;
    gap: 48px $comics-gap;

    margin-bottom: 24px;
}

.btn-container {
    text-align: center;
    padding: 24px 0;
}

</style>