<!-- eslint-disable vue/no-multiple-template-root -->
<!-- eslint-disable vue/multi-word-component-names -->
<!-- Esta es la lista de preguntas y el componente del primer radio button -->
<template>
    <ul id="object" class="demo">
        <aside class="title">{{pregunta}}</aside>        
        <li v-for="pregunta in objects" v-bind="objects" class="listOption" :key="pregunta.id">
            <input class="radio" type="radio" v-model="selectOption" name="option" v-bind:id="pregunta.id">
            <label v-bind="pregunta">{{ pregunta.question }}</label>
        </li>
    </ul>
    </template>

<script>
// import Ofert from './components/Option.vue'
import ButtonComponent from './ButtonComponent.vue';


export default {
    name: 'FirstQuestion',
    data() {
        return {
            elementId: '#object',
            selectOption:null,
            checked: false,
            components: {
                ButtonComponent
            },
            pregunta: 'Pregunta 1',
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
.title{
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
    background-color: blue;
    display: flex;
    align-items: flex-start;
    font-size: 33px;
    padding: 10px;
}
</style>
  