<template>
    <div>
        <h1>Fournisseur : {{ name }}</h1>
        <h5 v-if="status" :class="'green'">A du stock: OK</h5>
        <h5 v-else :class="'red'">A du stock: KO</h5>
        <h3>Date de la derniere levée: {{ checkedAt }}</h3>
    </div>
</template>

<script>
    export default {
        name: "Supplier",
        props:{
            id: Number,
            name: String,
            status: Boolean,
            checkedAt: String,
        }
    }
</script>

<style scoped>
    .green{ color: mediumseagreen; }
    .red{ color: orangered; }
</style>