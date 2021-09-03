<template>
    <div>
        <h2>Belajar Two Data Binding</h2>

        <h5>Pesan : {{ pesan }}</h5>
        <input v-model="pesan">
    </div>
</template>


<script>
export default {
    data(){
        return{
            pesan: '',
        }
    }
}
</script>