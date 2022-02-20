<template>
  <div>
    <h2>MONEDAS</h2>

    <input v-model="valorEntrada" type="number" placeholder="ingrese cantidad"/>
    <select v-model="unidadEntrada" name="listaUnidades">
      <option value="0.04928">Pesos Mexicanos</option>
      <option value="1.13164">Euro Europa</option>
      <option value="1">Dolar Americano</option>
      <option value="0.00936">Pesos Argentinos</option>
      <option value="0.00025">Pesos Colombianos</option>
      <option value="38329.05115">Bitcoin</option>


    </select>
    <span> convertir a </span>
    <select v-model="unidadSalida" name="listaUnidades">
      <option value="0.04928">Pesos Mexicanos</option>
      <option value="1.13164">Euro Europa</option>
      <option value="1">Dolar Americano</option>
      <option value="0.00936">Pesos Argentinos</option>
      <option value="0.00025">Pesos Colombianos</option>
      <option value="38329.05115">Bitcoin</option>

    </select>

    <b-button variant="success" v-on:click="CalcularMoneda" title="Convertir" >Convertir</b-button>
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
  name: "ConversorMoneda",
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
    CalcularMoneda() {
      this.resul = (this.unidadEntrada / this.unidadSalida) * this.valorEntrada;
      this.UnidDeEntrada = (this.valorEntrada)
      console.log(this.valorEntrada);
      console.log(this.unidadEntrada)
      console.log(this.unidadSalida)
    }
  }
};
</script>
