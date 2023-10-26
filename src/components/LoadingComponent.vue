
<!-- este componente es el del proceso de carga de la app -->
<template>
  <!-- <div class="loading">
    <aside class="aside">
      Progreso:
    </aside>
      <p class="porcent"> </p>
      
    </div> -->
    <Progress :value="currentProgress" />

  </template>
  
  <script>
  export default {
    name: 'LoadingComponentVue',
    props: {
      counter:Number, 
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  .loading {
    background-color: white;
    width: 100%;
    border: 0.5px solid black;
  }
  .aside {
    width: 100px;
    height: 15px;position: absolute;
    margin: 20px;
    margin-left: 30px;
    background-color: white;
    color: black;

  }
  
  .porcent {
    background-color:rgba(194, 44, 187, 0.948) ;
    width: 167px; 
    height: 15px;
    margin: 40px;
    margin-top: 50px;
    border-radius:40px;
  }
  /* el ancho maximo es de 500 /3 = 167 */
  </style>
  