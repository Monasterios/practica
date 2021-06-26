<template>
  <div class="hello">
    {{ msg }}

    <Hermano v-model:title="nuevaVariable"/>
    <Hermano v-model:title="funcionComputada"/>

    {{nuevaVariable}}
    <Padre :msg="arrays"/>
  </div>
</template>

<script>

import Padre from "./Padre";
import Hermano from "./Hermano";

export default {
  name: 'Abuelo',
  components: {Hermano, Padre},
  props: {
    msg: String
  },
  data() {
    return {
      namePadre: this.msg,
      nuevaVariable: 'caracol',
      cambia:'w2121',
      arrays: [
        {nombre: 'Guillermo', edad: 33, pais: 'Venezuela'},
        {nombre: 'David', edad: 25, pais: 'Austria'},
        {nombre: 'Gustavo', edad: 42, pais: 'España'}
      ]
    }
  },
  computed: {
     funcionComputada () {
       return this.nuevaVariable
     }
  },
  watch: {
    nuevaVariable() {
       console.log('esta cambiando la variable')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
