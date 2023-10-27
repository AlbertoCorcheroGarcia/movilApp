<!-- eslint-disable vue/no-multiple-template-root -->
<!-- eslint-disable vue/multi-word-component-names -->
<!-- Esta es la lista de preguntas y el componente del primer radio button -->
<template>
  <div class="containerTelephone">
    <input type="number"  class="telephone" placeholder="Telefono" v-model="inputValue" />
    <button class="buttonTelephone">FINALIZAR</button>
  </div>
</template>

<script>
// import Ofert from './components/Option.vue'


export default {
    name: 'TelephoneComponent',

    methods: {
    

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
                
            },
           

        
        };
    }
}
</script>
  

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.containerTelephone{
    display: flex;
    flex-direction: row;
    justify-content: flex-end;}

.telephone{
    width: 410px;
    height: 50px;
    margin-top: 100px;
    border-radius: 40px;
    font-size: 25px;
    text-align: center;
    color: white;
}
.buttonTelephone{
    width: 10%;
    height: 55px;
    background-color: rgba(232, 68, 226, 1);
    border-radius: 30px;
    font-size: 15px;
    position: absolute;
    top: 1258px;
    color: white;;
    
}
</style>
  