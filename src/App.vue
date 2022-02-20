<template>
  <div id="app">
    <carrucel/>
    <br>
    <br>
    <center>
    <img alt="TargarienLogo" align="middle" width="200" src="https://i.pinimg.com/originals/3d/68/8f/3d688fa74af883979bb19865d743516b.png" />
    </center>
    <br>
    <br>
    <conversor-masa />
    <conversor-longitud/>
    <conversor-almacenamiento/>
    <conversor-tiempo/>
    <conversor-moneda/>
  </div>
</template>

<script>
import ConversorMasa from "./components/ConversorMasa.vue";
import ConversorLongitud from "./components/ConversorLongitud.vue";
import ConversorAlmacenamiento from "./components/ConversorAlmacenamiento.vue";
import ConversorTiempo from "./components/ConversorTiempo.vue";
import ConversorMoneda from "./components/ConversorMonedas.vue";
import Carrucel from "./components/Carrucel.vue";
export default {
  name: "App",
  components: {
    Carrucel,
    ConversorMasa,
    ConversorLongitud,
    ConversorAlmacenamiento,
    ConversorTiempo,
    ConversorMoneda,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
