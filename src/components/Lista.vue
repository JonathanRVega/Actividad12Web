<template>
  <div class="container">
    <table class="table">
      <tbody>
        <tr v-for="(item, index) in chuck" :key="index">
          <td class="index-number">{{ index + 1 }}</td>
          <td class="text-column">{{ item.value }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "ActividadList",
  data() {
    return {
      chuck: [
        { value: "Chuck Norris can skydive into outer space." },
        { value: "The chief export of Chuck Norris is pain." },
        { value: "Chuck Norris doesn't read books. He stares them down until he gets the information he wants." },
        { value: "Time waits for no man. Unless that man is Chuck Norris." },
        { value: "If you spell Chuck Norris in Scrabble, you win. Forever." },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  margin: 20px;
}

.table {
  width: 80%;
  border-collapse: collapse;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border: 1px solid #ddd;
  background-color: #f9f9f9;
}

.table td {
  padding: 10px;
  border-bottom: 1px solid #ddd;
}

.table tr:hover {
  background-color: #f1f1f1;
}

.index-number {
  text-align: center;
  font-weight: bold;
  color: #555;
}

.text-column {
  font-size: 1rem;
  color: #333;
}

</style>