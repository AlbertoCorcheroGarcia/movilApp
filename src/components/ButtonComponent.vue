<!-- eslint-disable vue/no-parsing-error -->
<!-- eslint-disable vue/multi-word-component-names -->
<!-- Esta es la lista de preguntas y el componente del primer radio button -->
<template>
    <div>
        <button v-if="selectOption == false" class="buttOn" v-on:click="isClicked"></button>
        <button v-else-if="this.counter == 1" class="buttOn2" v-on:click="isClicked"></button>
        <button v-else  class="buttOff" v-on:click="isClicked " :disabled="this.counter == 2"><i class="fa fa-cloud cloud"></i>
</button>
    </div>
</template>
   
<script>
// import Ofert from './components/Option.vue'

export default {
    name: 'ButtonComponentVue',

    methods: {
        isClicked() {
            this.selectOption = +1            
            console.log(this.selectOption,"seleccionado, is cliked ");
            console.log(this.counter,"counter");
            this.counter = this.counter + 1
            return  this.selectOption
        }
 
    },
    props: {
        msg: String
    },
    data() {
        return {
            counter: 1,
            selectOption: false,
            elementId: '#button',

        };
    }
}
</script>
     
   
     <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.buttOn {
    background-color: rgb(87, 142, 101);
    width: 70px;
    height: 60px;
    display: flex;
    border-radius: 20px;
}

.buttOn:focus {
    background-color: rgb(43, 255, 0);
    transition: 1s;
}

.buttOff {
    background-color: rgb(0, 250, 108);
    width: 400px;
    height: 75px;
    display: flex;
    border-radius: 20px;
    transition: 4s;
}
.cloud{
    background-color: rgb(0, 250, 108);
    font-size: 30px;
    margin-left:50px ;
    margin-top:12px ;
    transition: 1s;
    color: black;
}

</style>
     