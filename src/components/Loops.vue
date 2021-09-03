<template>
  <div>
    <h4>Belajar Looping vue js</h4>

    <table border="1">
      <tr v-for="hari in namaHari" v-bind:key="hari">
        <th>
            {{hari}}
        </th>
      </tr>
      
      <tr>
          <td>{{ hari }}</td>
      </tr>
    </table>
  </div>
</template>
<script>
export default {
  data() {
    return {
      namaHari: [
        "Senin",
        "Selasa",
        "Rabu",
        "Kamis",
        "Jumat",
        "Sabtu",
        "Minggu",
      ],
    };
  },
};
</script>
