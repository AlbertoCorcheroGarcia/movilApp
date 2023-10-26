<!-- eslint-disable vue/multi-word-component-names -->
<!-- Esta es la lista de preguntas y el componente del primer radio button -->
<template>
    <ul id="v-for-option" class="demo">
       <li v-for="pregunta in objects" v-bind="object" :key="pregunta.id">
           <input type="checkbox" name="option" v-bind:id="pregunta.id">
           <label v-bind:for="pregunta.id">{{pregunta.question}}</label>
   
       </li>
   </ul>
   </template>
   <!-- las props aqui no son reactivas  -->
   
   <script>
   
   export default {
       name: 'OptionRadioComponentVue',
       data() {
           return {
               elementId: '#v-for-option',
               objects: [
                   { id: 1, question: 'Opcion 1' },
                   { id: 2, question: 'Opcion 2' },
                   { id: 3, question: 'Opcion 3' },
                   { id: 4, question: 'Opcion 4' },
               ],
           };
       }}
   </script>
     
   
     <!-- Add "scoped" attribute to limit CSS to this component only -->
   <style scoped>
   
   .demo{
       background-color: rgb(0, 174, 255);
       width: 100px;
       height: 100px;
       list-style:none;
       
   }
   </style>
     