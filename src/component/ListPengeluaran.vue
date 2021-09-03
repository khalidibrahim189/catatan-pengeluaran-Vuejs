<template>
  <div class="container">
    <table class="table table-bordered mt-5">
      <thead>
        <tr class="bg-danger text-white">
          <th scope="col">Nominal</th>
          <th scope="col">Keterangan</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(pengeluaran, index) in dataPengeluaran" :key="index">
          <td>{{ pengeluaran.nominal }}</td>
          <td>{{ pengeluaran.keterangan }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    dataPengeluaran: Array,
  },
};
</script>
