<template>
  <Title title="Catatan Pengeluaran" />
  <FormPengeluaran @entri-pengeluaran="entriPengeluaran($event)" />
  <h2>Total Pengeluaran : {{ total_pengeluaran }}</h2>
  <ListPengeluaran
    v-if="tampilData"
    :dataPengeluaran="dataPengeluaran"
  />
</template>

<script>
import Title from "./component/Title.vue";
import ListPengeluaran from "./component/ListPengeluaran.vue";
import FormPengeluaran from "./component/FormPengeluaran.vue";
// import func from 'vue-editor-bridge';

export default {
  name: "App",
  components: {
    Title,
    ListPengeluaran,
    FormPengeluaran,
  },
  data() {
    return {
      dataPengeluaran: [
        // {
        //   nominal: 10000,
        //   keterangan: "Beli Sabun",
        // },
        // {
        //   nominal: 5000,
        //   keterangan: "Beli Salome",
        // },
        // {
        //   nominal: 10000,
        //   keterangan: "Beli Teh Botol Sosro",
        // },
        // {
        //   nominal: 15000,
        //   keterangan: "Beli Kuota",
        // },
      ],
    };
  },

  methods: {
    entriPengeluaran(event) {
      this.dataPengeluaran.push(event);
    },
  },

  computed: {
    tampilData: function() {
      return this.dataPengeluaran.length > 0;
    },
    total_pengeluaran: function(){
      return this.dataPengeluaran.reduce((accum, item) => accum+parseInt(item.nominal), 0);
    }
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
