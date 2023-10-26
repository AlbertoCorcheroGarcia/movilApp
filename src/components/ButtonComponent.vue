<!-- eslint-disable vue/multi-word-component-names -->
<!-- Esta es la lista de preguntas y el componente del primer radio button -->
<template>
    <button class="buttOn"></button>
</template>
   
<script>
// import Ofert from './components/Option.vue'

export default {
    name: 'ButtonComponentVue',
    data() {
        return {
            selectOption:null,
            elementId: '#button',

        };
    }
}
</script>
     
   
     <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.buttOn {
    background-color: rgb(0, 174, 255);
    width: 60px;
    height: 60px;
    /* list-style:none; */

}
</style>
     