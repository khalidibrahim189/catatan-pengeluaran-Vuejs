<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <form @submit.prevent="tambah">
          <div class="container">
            <div class="form-group">
              <input
                type="number"
                v-model="pengeluaran"
                name="pengeluaran"
                class="form-control"
                placeholder="Masukan Nominal anda"
                id="pengeluaran"
              />
            </div>
            <div class="form-group mt-3">
              <input
                type="text"
                v-model="keterangan"
                name="keterangan"
                class="form-control"
                placeholder="Masukan Keterangan anda"
                id="keterangan"
              />
            </div>

            <button class="btn btn-danger mt-3">Tambah</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pengeluaran: null,
      keterangan: null,
    };
  },
  methods:{
      tambah(){
          this.$emit('entri-pengeluaran',{
              nominal: this.pengeluaran,
              keterangan : this.keterangan
          });

          this.pengeluaran = null;
          this.keterangan = null;
          document.getElementById("pengeluaran").focus()
      }
  }
};
</script>

<style scoped>

</style>
