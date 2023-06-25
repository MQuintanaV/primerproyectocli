<template>
  <div class="home">
    <img src="" alt="">
    <button v-on:click="cargarTomioka">ver a Tomioka</button>
    <button v-on:click="cargarTokito">ver a Tokito</button>
    <hr>
    <img alt="textoMostrar" v-bind:src="imagenMostrar">
    <HelloWorld msg="KIMETSU NO YAIBA"/>
    
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },
  data:function(){
    return{
      imagenTomioka:'./assets/img/tomioka.jpg',
      imagenTokito:'./assets/img/tokito.jpg',
      imagenMostrar:'',
      textoMostrar:'no hay imagen seleccionada'
    }
  },
  methods:{
    cargarTomioka: function(){
      this.imagenMostrar = this.imagenTomioka;
      this.textoMostrar= 'tomioka';

    },
    cargarTokito: function(){
      this.imagenMostrar = this.imagenTokito
    
  }
}
}
</script>
<style scoped>
.home{
  background-color: lightgreen;
}
</style>
