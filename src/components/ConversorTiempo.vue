<template>
  <div>
    <h2>TIEMPO</h2>

    <input v-model="valorEntrada" type="number" placeholder="ingrese cantidad"/>
    <select v-model="unidadEntrada" name="listaUnidades">
      <option value="1440">dias</option>
      <option value="60">Horas</option>
      <option value="1">Minutos</option>
      <option value="525960">Años</option>
      <option value="43830">Meses</option>
      <option value="1.0080">Semanas</option>


    </select>
    <span> convertir a </span>
    <select v-model="unidadSalida" name="listaUnidades">
      <option value="1440">dias</option>
      <option value="60">Horas</option>
      <option value="1">Minutos</option>
      <option value="525960">Años</option>
      <option value="43830">Meses</option>
      <option value="1.0080">Semanas</option>

    </select>

    <b-button variant="success" v-on:click="CalcularTiempo" title="Convertir" >Convertir</b-button>
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
  name: "ConversorTiempo",
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
    CalcularTiempo() {
      this.resul = (this.unidadEntrada / this.unidadSalida) * this.valorEntrada;
      this.UnidDeEntrada = (this.valorEntrada)
      console.log(this.valorEntrada);
      console.log(this.unidadEntrada)
      console.log(this.unidadSalida)
    }
  }
};
</script>
