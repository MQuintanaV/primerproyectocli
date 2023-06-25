<template>
  <div class="about">
    <h1>Kimetsu no yaiba</h1>
    <p>La obra sigue las aventuras de Tanjirō Kamado, un adolescente cuya familia fue cruelmente asesinada por un Demonio el cual convirtió a su hermana Nezuko en una de estas criaturas, obligando a Tanjirō a emprender un viaje para cazar a estos seres y de paso ayudar a su hermana a recuperar su humanidad.</p>

    <p>{{ texto }}</p>
    <p>{{ despedida }}</p>
    <input type="text" v-bind:value="contenidoTexto"><br>
    <button v-on:click="despedirse">ver despedida</button>
  </div>
  
</template>
<script>
  export default{
    name:'about-component',
    data: function(){
      return{
        texto:'esto es texto de modelo de datos',
        despedida:'',
        contenidoTexto: 'contenido viene del modelo'
      }
    },
    methods:{
      despedirse: function(){
        this.despedida ='me voy mañana sigo'
      }
    }
  }
</script>

<style scoped>
.about{
  background-color: lightcoral;
}
</style>