<template>
    <div class="container">
        <h1 class="title">
            Daily Cat Fact <figcaption></figcaption>
        </h1>
        <div class="card">
            <div class="card-body">
                <h2 class="fact-content"> {{ catFact }}</h2>
                <button class="btn btn-primary" @click="getCatFact">More Facts</button>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        name: "CatFact",
        data() {
            return {
                catFact: ''
            }
        },
        methods: {
            async getCatFact() {
                const response = await fetch("https://cat-fact.herokuapp.com/facts/random")
                const jsonData = await response.json()
                this.catFact = jsonData.text
            }
        },
        mounted() {
            this.getCatFact()
        }
    }
</script>
<style scoped>
    .container {
        padding-top: 10px;
    }
    .title {
        margin-top: 100px;
        color: azure;
    }
    .fact-content {
        color: black
    }
    .card {
        width: 800px;
        margin: auto;
    }
    .card-body {
        background-color:azure;
    }
</style>