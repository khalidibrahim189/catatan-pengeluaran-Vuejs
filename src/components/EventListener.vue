<template>
    <div>
        <h2>Belajar EventListener Vue js</h2>

        <h3>Deret Bilangan Genap</h3>
        <h3>Angka : {{ angka }}</h3>
        <button v-on:click="next">Next</button>

        

    </div>
</template>


<script>
export default {
    data(){
        return{
            angka : 1
        }
    },

    methods:{
        next(){
            this.angka +=2;
        }
    }
}
</script>