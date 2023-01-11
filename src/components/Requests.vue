<template>
  <div>
    <h1>{{ headline }}</h1>
    <table>
      <tr>
        <th>Name</th>
        <th>Postleitzahl</th>
        <th>Zählpunkt</th>
        <th>kwPeak</th>
        <th>bewilligt</th>
      </tr>
      <tr v-for="pv in data">
        <td>{{ pv.name }}</td>
        <td>{{ pv.plz }}</td>
        <td>{{ pv.zaehlpunkt }}</td>
        <td>{{ pv.kwPeak }}</td>
        <td>
          <input
            type="checkbox"
            id="checkbox"
            v-model="pv.bewilligt"
            @change="handleChange"
          />
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Requests',
  props: {
    headline: String,
    data: { type: Array },
  },
};
</script>

<style scoped>
h1 {
  background-color: aqua;
}
table,
th,
td {
  text-align: center;
  border: 1px solid black;
  padding: 3px;
}
</style>
