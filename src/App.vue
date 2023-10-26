<!-- eslint-disable no-unused-vars -->
<!-- Este es el componente principal -->
<template>
  <div id="app">
    <LoadingComponentVue v-bind="{ counter }" @cchanged="ifChecked = $event"  class="loading" >Progreso</LoadingComponentVue>
    
    <div id="containerOfer">
      <Ofert class="oferta" :msg="'Oferta del mes'" />
      <Ofert class="descuento" :msg="'50% de descuento'" />
    </div>
    <div class="questionComponent">
      <FirstQuestion class="firstQuestion" :v-props="{ checked: true }" v-if="checked==false"/>

      <ButtonComponent class="buttonComponent"  />
    </div>

    <div class="option" objects="object" >
    
    </div>
    <!-- <OptionRadioComponentVue /> -->
  </div>
</template>

<script>
// import OptionRadioComponentVue from './components/OptionRadioComponent.vue'
import LoadingComponentVue from './components/LoadingComponent.vue'
import Ofert from './components/Ofert.vue'
import FirstQuestion from './components/FirstQuestion.vue'
import ButtonComponent from './components/ButtonComponent.vue'

export default {
  name: 'App',
  props: {
    msg: String,
    objects: Array,
    checkBox: Boolean,
    checked: Boolean,
    counter:Number
  },
  components: {
    LoadingComponentVue,
    Ofert,
    FirstQuestion,
    ButtonComponent,
    // OptionRadioComponentVue,

  }
  ,watchers: {
    ifChecked(){
      return this.checked
    }
  
  },
  computed: {
   
    
  }
}
</script>

<style>
* {
  background-color: black;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
  margin-left: 300px;
  margin-right: 300px;
  height: 100%;
  width: 600px;
  background-color: white;
  border-radius: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.loading {
  background-color: red;
  width: 100%;
  height: 100px;
  border-radius: 20px 20px 0 0;

}
.oferta {
  font-size: 9px;
}




#containerOfer {
  background-color: rgb(212, 92, 245);
  margin-bottom: 50px;
  margin-top: 10px;
  width: 80%;
  height: 80%;
  border-radius: 20px;
  
}

.option {
  background-color: yellow;
  width: 500px;
  height: 400px;
  margin-bottom: 30px;
  display: flex;
  border: solid black 3px;
}

.firstQuestion {
  background-color: black;
  width: 500px;
  border-radius: 20px;
}
.questionComponent{
  background-color: green;
  
}
.buttonComponent {
background-color: red;
  display: flex;

  }
</style>
