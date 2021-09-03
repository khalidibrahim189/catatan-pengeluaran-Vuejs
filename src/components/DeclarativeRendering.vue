<template>
    <div>
        <h2>Belajar Declarative Rendering</h2>


        <h5>Nama : {{ nama }}</h5>
        <h5>Umur : {{ umur }}</h5>
    </div>
</template>


<script>
export default {
    data(){
        return{
            nama : "Khalid Ibrahim",
            umur : 20
        }
    },


    mounted(){
        this.umur = this.umur + 2;
    }
}
</script>