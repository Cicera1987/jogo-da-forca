<template>
    <div class="forca">
        <img :src="`https://raw.githubusercontent.com/william-costa/wdev-hangman-game-resources/master/images/hangman/${erros}.svg`"
            alt="forca">


    </div>
</template>

<script>

export default {
    name: 'ForcaView',
    props: {
        erros: Number,

    },
    data() {
        return {

        }
    },
    methods: {

    },
}



</script>

<style >
.forca img {
    width: 150px;

}
</style>