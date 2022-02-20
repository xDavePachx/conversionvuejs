<template>
  <div>
    <h2>LONGITUD</h2>

    <input v-model="valorEntrada" type="number" placeholder="ingrese cantidad"/>
    <select v-model="unidadEntrada" name="listaUnidades">
      <option value="1609.34">Milla</option>
      <option value="1000">Kilometro</option>
      <option value="1">Metro</option>
      <option value="0.001">Milimetro</option>
      <option value="0.9144">Yarda</option>

    </select>
    <span> convertir a </span>
    <select v-model="unidadSalida" name="listaUnidades">
      <option value="1609.34">Milla</option>
      <option value="1000">Kilometro</option>
      <option value="1">Metro</option>
      <option value="0.001">Milimetro</option>
      <option value="0.9144">Yarda</option>

    </select>

    <b-button variant="success" v-on:click="CalcularLongitud" title="Convertir" >Convertir</b-button>
    <br>
    <br>
    <h4>{{UnidDeEntrada}} Esto equivale a: {{resul}}</h4>
    <br>
    <br>
    <br>
    <br>
  </div>
</template>
<script>
export default {
  name: "ConversorLongitud",
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
    CalcularLongitud() {
      this.resul = (this.unidadEntrada / this.unidadSalida) * this.valorEntrada;
      this.UnidDeEntrada = (this.valorEntrada)
      console.log(this.valorEntrada);
      console.log(this.unidadEntrada)
      console.log(this.unidadSalida)
    }
  }
};
</script>
