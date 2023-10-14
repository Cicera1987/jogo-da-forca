<template>
    <div class="final">
        <div :class="`final-texto ${etapa}`">
            {{ texto }}

            <button class="fininal-button" v-on:click="reiniciar">Jogar novamente</button>
        </div>

    </div>
</template>

<script>


export default {
    name: 'FinalView',
    props: {
        etapa: String,
        texto: String,
        reiniciar: Function

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
.final-texto {
    margin: 20px 0px;
    font-size: 24px;
    font-weight: bold;
}

.final-texto.enforcado {
    color: var(--color-text-error);
}

.final-texto.ganhador {
    color: var(--color-text-success);
}
</style>