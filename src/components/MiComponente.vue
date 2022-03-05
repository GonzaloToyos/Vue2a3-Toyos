<template>
  <table :style="estilo">
    <tr v-for="(row, prop) of msg" :key="row" :style="color(prop)">
      <td v-for="valor of row" :key="valor">{{ valor }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  name: "TablaEjercicio",
  props: {
    msg: Array,
    text: String,
    bgp: String,
    bgs: String,
  },
  data() {
    return {
      estilo: this.text + "; " + "border-collapse:collapse; font-size: 24px",
    };
  },
  methods: {
    color(i) {
      let result = i%2 ? this.bgp : this.bgs;
      return result;
    },
  },
};
</script>

<style scoped>
table {
  margin-bottom: 15px;
}
</style>