<template>
    <div class="palavra">
        <div class="letras">
            <div class="palavra-letra" v-for="(letra, key) in palavra" :key="key">
                {{ (verificaLetra(letra)) || etapa === 'enforcado' ? letra : '' }}
            </div>
        </div>
        <div class="dica">
            <p>{{ dica }}</p>
        </div>


    </div>
</template>

<script>


export default {
    name: 'PalavraView',
    props: {
        palavra: String,
        dica: String,
        verificaLetra: Function,
        etapa: String
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
.palavra {
    text-transform: uppercase;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.letras {
    display: flex;
    margin-bottom: 20px;
}

.palavra-letra {
    height: 30px;
    width: 30px;
    margin: 0 5px;
    border-bottom: 1px solid var(--color-text-light);
    display: flex;
    justify-content: center;
    align-items: center;

}
</style>