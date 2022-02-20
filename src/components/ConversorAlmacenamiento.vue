<template>
  <div>
    <h2>ALMACENAMIENTO</h2>

    <input v-model="valorEntrada" type="number" placeholder="ingrese cantidad"/>
    <select v-model="unidadEntrada" name="listaUnidades">
      <option value="1">Byte</option>
      <option value="1024">Kilobyte</option>
      <option value="1048576">Megabyte</option>
      <option value="1073741824">Gigabyte</option>
      <option value="1099511627776">Terabyte</option>

    </select>
    <span> convertir a </span>
    <select v-model="unidadSalida" name="listaUnidades">
      <option value="1">Byte</option>
      <option value="1024">Kilobyte</option>
      <option value="1048576">Megabyte</option>
      <option value="1073741824">Gigabyte</option>
      <option value="1099511627776">Terabyte</option>


    </select>

    <b-button variant="success" v-on:click="CalcularAlmacenamiento" title="Convertir" >Convertir</b-button>
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
  name: "ConversorAlmacenamiento",
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
    CalcularAlmacenamiento() {
      this.resul = (this.unidadEntrada / this.unidadSalida) * this.valorEntrada;
      this.UnidDeEntrada = (this.valorEntrada)
      console.log(this.valorEntrada);
      console.log(this.unidadEntrada)
      console.log(this.unidadSalida)
    }
  }
};
</script>
