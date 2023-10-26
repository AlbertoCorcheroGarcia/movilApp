<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <!-- este componente es el que saca el mensaje de 50% de descuento  -->

    <!-- este componente no da fallos  -->

  </div>
</template>

<script>
export default {
  name: 'OferTitle',
  props: {
    msg: String
  },
  msg:"50% de descuento"
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.hello {
  background-color: rgb(212, 92, 245);
  border-radius: 20px;


  
}

h1 {
  background-color: rgb(212, 92, 245);
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  margin-left: 15px;
  border-radius: 20px;

  
    
  }
ul {
  list-style-type: none;
  padding: 0;
}
li {  
  display: inline-block;
  margin: 0 10px;
}
</style>
