<template>
    <div class="formulario">
        <div class="formulario-title">{{ title }} </div>
        <input type="text" class="input" v-model="palavra">
        <button :disabled="palavra.length === 0" class="button" v-on:click="onsubmit">{{ button }}</button>
    </div>
</template>

<script>

export default {
    name: 'InitialView',
    props: {
        title: String,
        button: String,
        action: Function,
    },
    data() {
        return {
            palavra: '',
        }
    },
    methods: {
        onsubmit: function () {
            this.action(this.palavra);
            this.palavra = '';
        }
    },
}



</script>

<style scoped> .formulario {
     display: flex;
     flex-direction: column;
     align-items: center;
     justify-content: center;
     text-align: center;
     margin-top: 20px;
 }

 .formulario-title {
     font-size: 20px;
     font-weight: bold;
     margin-bottom: 20px;
 }

 .input {
     padding: 10px 5px;
     box-shadow: 0;
     border: 0 none;
     outline: 0;
     border-radius: 5px;
     margin: 10px 0;
     text-align: center;
     color: var(--color-text-dark);



 }
</style>