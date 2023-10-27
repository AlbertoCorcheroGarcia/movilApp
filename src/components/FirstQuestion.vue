<!-- eslint-disable vue/no-multiple-template-root -->
<!-- eslint-disable vue/multi-word-component-names -->
<!-- Esta es la lista de preguntas y el componente del primer radio button -->
<template>
    <ul id="object" class="demo">
        <aside class="title">{{ texto }}</aside>

        <li v-for="pregunta in objects" v-bind="objects" class="listOption" @click="isSelected()" :key="pregunta.id">
            <input :disabled="selectOption==1" class="radio" v-model="selectOption" type="radio" name="option" >
            <label v-bind="selectOption">{{ pregunta.question }}</label>
        </li>

    </ul>
</template>

<script>
// import Ofert from './components/Option.vue'
import ButtonComponent from './ButtonComponent.vue';


export default {
    name: 'FirstQuestion',

    methods: {
    

        log() {
            console.log(this.selectOption);
            console.log(this.selectOption);
            console.log(this.opcionSelecionada);
            
        },
        isSelected() {
            this.selectOption=+1
            console.log(this.selectOption,"seleccionado, is cliked ");
            return this.selectOption
        },
    },

    watchers: {
      
     

    },
    data() {
        return {
            elementId: '#object',
            selectOption: null,
            // le pongo una propiedad de si esta marcado o no el boton , por defecto esta en falso 
            // checked: false,
            components: {
                ButtonComponent
            },
            texto: 'Pregunta 1',
            objects: [
                { id: 1, question: 'Opcion 1' },
                { id: 2, question: 'Opcion 2' },
                { id: 3, question: 'Opcion 3' },

            ],
        };
    }
}
</script>
  

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.demo {
    /* background-color: red; */
    width: 500px;
    height: 300px;
    list-style: none;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 10px;


}
label {

    background-color: white;
    color: black;
}

.title {
    display: flex;
    width: 300px;
    height: 70px;
    font-size: 50px;
    background-color: white;
    color: black;
}

.radio {
    width: 900px;
    height: 30px;
    display: flex;
    position: absolute;
}

.listOption {
    background-color: white;
    display: flex;
    align-items: flex-start;
    font-size: 33px;
    padding: 10px;
}
</style>
  