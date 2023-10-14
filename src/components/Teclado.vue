<template>
    <div class="teclado">
        <button class="teclado-botao" 
        v-for="(letra, key) in 'abcdefghijklmnopqrstuvwxyz'" 
        :key="key"
        :disabled="verificaLetra(letra)" 
        v-on:click="jogar(letra)"
        >{{ letra }}</button>

    </div>
</template>

<script>


export default {
    name: 'TecladoView',
    props: {
        letras: Array,
        verificaLetra: Function,
        jogar: Function
    },
    data() {
        return {

        }
    },
    methods: {

    },
    components: {

    }
}


</script>

<style>
.teclado {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 345px;
    margin-top: 20px;

}

.teclado-botao {
    margin: 5px;
    text-transform: uppercase;
    background-color: #000;
}
</style>