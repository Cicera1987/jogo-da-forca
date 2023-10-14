<template>
    <div class="jogo">
        <Forca 
        :erros="erros"
        />
        <Palavra
        :palavra="palavra"
        :dica="dica"
        :verificaLetra="verificaLetra"
        :etapa="etapa"
        />
        <Teclado
        v-if="etapa === 'jogo'"
        :letras = "letras"
        :verificaLetra="verificaLetra"
        :jogar="jogar"
        />
        <Final
        v-if="etapa != 'jogo'"
        :etapa="etapa"
        :texto="etapa === 'ganhador' ? 'Parabéns, você ganhou :) !' : 'Que pena, você perdeu :( !'"
        :reiniciar="reiniciar"
        />

    </div>
</template>

<script>

import Forca from './Forca'
import Palavra from './Palavra'
import Teclado from './Teclado'
import Final from './Final'

export default {
    name: 'JogoView',
    props: {
        erros: Number,
        palavra: String,
        dica: String,
        verificaLetra: Function,
        etapa: String,
        letras: Array,
        jogar: Function,
        reiniciar: Function

    },
    data() {
        return {


        }
    },
    methods: {

    },
    components: {
        Forca,
        Palavra,
        Teclado,
        Final
    }
}


</script>

<style>
.jogo {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}
</style>