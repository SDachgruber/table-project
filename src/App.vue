<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <TableComponent
      msg="Table Compponent"
      :header="['A', 'B']"
      :bodydata="tableBodyContent"
    />
  </div>
</template>

<script>
import TableComponent from "./components/Table.vue";

export default {
  name: "App",
  components: {
    TableComponent,
  },
  data() {
    return {
      tableBodyContent: [
        ["@", "µ"],
        ["", "€"],
      ],
    };
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
