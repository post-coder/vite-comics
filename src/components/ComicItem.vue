<script>

export default {
    name: 'ComicItem',

    props: {
        comic: Object,
    },
}

</script>

<template>

<div class="comic">

    <img :src="comic.thumb" alt="Action Comics" class="comic-cover">

    <span class="comic-title">
        {{ comic.series }}
    </span>

</div>


</template>

<style lang="scss">
@use '../styles/variables' as *;

.comic {
    width: calc(100% / 6 - $comics-gap / 6 * 5);


    .comic-cover {
        width: 100%;
        margin-bottom: 1em;

        // rendiamo l'immagine quadrata
        aspect-ratio: 1 / 1;
        object-fit: cover;
        object-position: top;
    }

    .comic-title {
        text-transform: uppercase;
        font-size: .9em;
    }
}

</style>