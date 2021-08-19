<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ header }}</h2>
    <table class="table">
      <thead>
        <tr>
          <th v-for="(column, index) in header" :key="index">{{ column }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(tablerowdata, index) in bodydata" :key="index">
          <td v-for="(column, indexColumn) in tablerowdata" :key="indexColumn">
            {{ column }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    header: Array,
    bodydata: Array,
  },
};
</script>

<style>
table {
  width: 100%;
  background: #f5f5f5;
}
th, td {
  padding: 0.25rem;
  text-align: center;
}

th {
    background: limegreen;
}

tbody {
    background: #ddd;
}

tbody tr:nth-child(odd) {
   background-color: #eee;
}

tbody tr:hover {
  background: #dcdcdc;
}
</style>
