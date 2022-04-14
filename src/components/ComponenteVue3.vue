<template>
  <table :style="estilo">
    <tr v-for="(row, prop) of msg" :key="row" :style="color(prop)">
      <td v-for="valor of row" :key="valor">{{ valor }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  name: "tablaComponente",
  props: {
    price: Number,
    msg: Array,
    text: String,
    bgp: String,
    bgs: String,
  },

  setup(props) {
    function color (i) {
        let result = i%2 ? props.bgp : props.bgs;
      return result;
    }

    const estilo = props.text + "; " + "border-collapse:collapse; font-size: 24px";

    return { color, estilo };
  },
};
</script>

<style scoped>
table {
  margin-bottom: 15px;
}
</style>