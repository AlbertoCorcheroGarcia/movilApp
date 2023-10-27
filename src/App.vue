<!-- eslint-disable no-unused-labels -->
<!-- eslint-disable no-unused-vars -->
<!-- Este es el componente principal -->
<template>
  <div id="app">
    <LoadingComponentVue v-if="counter == 1" onchange="isCounted()"  v-bind="{ counter }" 
    class="loading" ></LoadingComponentVue>
    <LoadingComponentVue v-if="counter == 2" onchange="isCounted()"  v-bind="{ counter }"
    class="loading2" ></LoadingComponentVue>

    <div id="containerOfer">
      <Ofert class="oferta" :msg="'Oferta del mes'" />
      <Ofert  class="descuento" :msg="'50% de descuento'" />
    </div>
    <div class="questionComponent">
      <FirstQuestion v-if="selectOption == 0" v-model="inputValue" class="firstQuestion"/>
      <FirstQuestion v-else v-model="inputValue" class="firstQuestion"/>
      <ButtonComponent  class="buttonComponent" />

      <!-- <ButtonComponent v-else :disabled="isDisabled" @click="updateInputValue" class="buttonComponent"/> -->
    </div>
    <div class="option" objects="object" >
    </div>
    <OptionRadioComponentVue class="firstQuestion"/>
    <ButtonComponent  class="buttonComponent" />
    <telephone-component class="telephoneComponent"/>

  </div>
</template>

<script>
import OptionRadioComponentVue from './components/OptionRadioComponent.vue'
import LoadingComponentVue from './components/LoadingComponent.vue'
import Ofert from './components/Ofert.vue'
import FirstQuestion from './components/FirstQuestion.vue'
import ButtonComponent from './components/ButtonComponent.vue'
import TelephoneComponent from './components/TelephoneComponent.vue'

export default {
  name: 'App',
  data() {
    return {
      inputValue:'',
      counter:1
      
    }
  },
  methods: {
    updateInputValue(){
      return this.inputValue
    },
    
  },
  props: {
    msg: String,
    objects: Array,
    checkBox: Boolean,
    checked: Boolean,
    selectOption:Boolean,
    selectOption2:Boolean,

  },
  components: {
    LoadingComponentVue,
    Ofert,
    FirstQuestion,
    ButtonComponent,
    OptionRadioComponentVue,
    TelephoneComponent

  }
  ,watchers: {
    ifChecked(){
      return this.checked
    },
 
  
  },
  computed: {
   
    
  },

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
  margin-bottom: 100px;
}

.loading {
  background-color: white;
  width: 100%;
  height: 100px;
  border-radius: 20px 20px 0 0;
}
.loading2 {
  background-color: white;
  width: 100%;
  height: 200px;
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


.firstQuestion {
  background-color: white;
  width: 500px;
  border-radius: 20px;
}
.questionComponent{
  background-color: white;
  
}
.buttonComponent {
  display: flex;
  justify-content: center;
  background-color: white;
  }
  .telephoneComponent{
    background-color: white;
    margin-bottom:50px ;
  }
</style>
