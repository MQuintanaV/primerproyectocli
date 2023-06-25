<template>
  <div id="app">
    <nav>
      <router-link to="/">Inicio</router-link> |
      <router-link to="/about">Informacion</router-link>
    </nav>
    <router-view/>
    <hr>
    <div class="prueba">
      <p>contenido:</p>
      <p id="parrafoMensaje">{{ mensaje }}</p>
      <button v-on:click="saludar">ver saludo</button>
      <p>{{ saludo }}</p>
    </div>
    <hr>
  </div>
</template>
<script>
  export default{
    name:'app-component',
    data: function() {
      return{
        mensaje: 'Hola Mundo con VueJs',
        otroMensaje:'Estamos trabajando con VueJs',
        saludo:''
      }
    },
    methods:{
      saludar: function(){
        this.saludo = 'cambiando una propiedad del modelo de datos';
      }
    }
  }

</script>
  
<style>
body{
  background-color: lightpink;
}

.prueba{
  background-color: lightgreen;
  color: blueviolet;
}
#parrafoMensaje{
  font-size: 30px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: blue;
}
</style>
