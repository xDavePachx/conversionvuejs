<template>
  <div>
    <h1>CONVERSOR VUEJS DE UNIDADES DE MEDIDA</h1>
    <br>
    <br>
    <br>
    <br>
    <h2>MASA</h2>

    <input v-model="valorEntrada" type="number" placeholder="ingrese cantidad"/>
    <select v-model="unidadEntrada" name="listaUnidades">
      <option value="1000">Kilogramo</option>
      <option value="1">Gramo</option>
      <option value="0.001">Miligramo</option>
      <option value="453.592">Libra</option>

    </select>
    <span> convertir a </span>
    <select v-model="unidadSalida" name="listaUnidades">
      <option value="1000">Kilogramo</option>
      <option value="1">Gramo</option>
      <option value="0.001">Miligramo</option>
      <option value="453.592">Libra</option>
    </select>

    <b-button variant="success" v-on:click="CalcularMasa" title="Convertir" >Convertir</b-button>
    <br>
    <br>
    <h4>{{UnidDeEntrada}} Esto equivale a: {{resul}}</h4>
    <br>
    <br>
    <br>
    <br>
    
    <!--<p>Resultado: <strong id="resultado"></strong></p>-->
  </div>
</template>
<script>
export default {
  name: "ConversorMasa",
  data() {
    return {
      valorEntrada:"",
      unidadEntrada:"",
      unidadSalida:"",
      resul:'',
      UnidDeEntrada:'',
    }
  },
  methods: {
    CalcularMasa() {
      this.resul = (this.unidadEntrada / this.unidadSalida) * this.valorEntrada;
      this.UnidDeEntrada = (this.valorEntrada)
      console.log(this.valorEntrada);
      console.log(this.unidadEntrada)
      console.log(this.unidadSalida)
      
    }
  }
};
</script>
