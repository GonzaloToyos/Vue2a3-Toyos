<template>
  <div id="app1">
    <div class="contenedor-tablas">
      <h3>Tabla Vue 2</h3>
      <TablaEjercicio
        :msg="miArray"
        :text="miColor"
        :bgp="bgPrimary"
        :bgs="bgSecondary"
      />
      <TablaEjercicio
        :msg="miArray2"
        :text="miColor2"
        :bgp="bgPrimary2"
        :bgs="bgSecondary2"
      />
      <TablaEjercicio
        :msg="miArray3"
        :text="miColor3"
        :bgp="bgPrimary3"
        :bgs="bgSecondary3"
      />
    </div>

    <div class="contenedor-tablas"> 
      <h3>Tabla Vue 3</h3>
      <tabla-componente
        :msg="miArray"
        :text="miColor"
        :bgp="bgPrimary"
        :bgs="bgSecondary"
      />
      <tabla-componente
        :msg="miArray2"
        :text="miColor2"
        :bgp="bgPrimary2"
        :bgs="bgSecondary2"
      />
      <tabla-componente
        :msg="miArray3"
        :text="miColor3"
        :bgp="bgPrimary3"
        :bgs="bgSecondary3"
      />
    </div>
  </div>
</template>

<script>
import TablaEjercicio from "./components/MiComponente.vue";
import tablaComponente from "./components/ComponenteVue3.vue";

export default {
  name: "App",
  components: {
    TablaEjercicio,
    tablaComponente,
  },
  data() {
    return {
      miArray: [
        { nombre: "Pedro", apellido: "Santos", edad: 35 },
        { nombre: "Marcelo", apellido: "Paez", edad: 43 },
        { nombre: "Juan", apellido: "Rutinger", edad: 23 },
        { nombre: "Alfredo", apellido: "López", edad: 15 },
        { nombre: "Mateo", apellido: "Sarmiento", edad: 30 },
      ],
      miColor: "color: white",
      bgPrimary: "background-color: rgb(33, 37, 41)",
      bgSecondary: "background-color: rgb(44, 48, 52)",
      miArray2: [
        { nombre: "Maria", apellido: "Frank", edad: 33 },
        { nombre: "Rigoberta", apellido: "Menchú", edad: 23 },
        { nombre: "Marta", apellido: "Palo", edad: 78 },
        { nombre: "Victoria", apellido: "Louz", edad: 34 },
        { nombre: "Anabella", apellido: "Simmons", edad: 40 },
      ],
      miColor2: "color: black",
      bgPrimary2: "background-color: rgb(209, 231, 221)",
      bgSecondary2: "background-color: rgb(199, 219, 210)",
      miArray3: [
        { nombre: "Rene", apellido: "Higuita", edad: 35 },
        { nombre: "Lionel", apellido: "Messi", edad: 36 },
        { nombre: "Julio", apellido: "Tolaymig", edad: 53 },
        { nombre: "Marco", apellido: "Polo", edad: 18 },
        { nombre: "Telesforo", apellido: "Ibarra", edad: 90 },
      ],
      miColor3: "color: black",
      bgPrimary3: "background-color: rgb(0, 255, 255)",
      bgSecondary3: "background-color: rgb(128, 255, 255)",
    };
  },
};
</script>

<style>
#app1 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  display: flex;
  justify-content: space-around;
}
</style>
