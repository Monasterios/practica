<template>
  <div class="Padre">
    <Hijo :msg="nameHijo"/>
    <ul v-for="(personas, index) in nameArreglo" :key="index">
      <li>{{personas.nombre}}</li>
    </ul>
  </div>
</template>

<script>
import Hijo from "./Hijo";
export default {
  name: 'Padre',
  components: {
    Hijo
  },
  props: {
    msg: Array
  },
  data () {
    return {
      nameHijo: ' ',
      nameArreglo: this.msg
    }
  },
  methods: {

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
