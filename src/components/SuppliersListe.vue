<template>
    <div>
        <h1>Liste de fournisseurs</h1>
        <div v-for="value in suppliers">
            <supplier v-bind:name="value.name" v-bind:status="value.status" v-bind:checked-at="value.checkedAt"></supplier>
        </div>
    </div>
</template>

<script>
    import Supplier from './Supplier'
    import { format, render, cancel, register} from 'timeago.js'
    export default {
        name: "SuppliersListe.vue",
        components:{ Supplier },
        data (){
            return {
                suppliers: [{
                    id: '1',
                    name: 'Frist-001',
                    status: false,
                    checkedAt: format(new Date().toLocaleString())
                },{
                    id: '2',
                    name: 'Second-002',
                    status: true,
                    checkedAt: format(new Date().toLocaleString())
                },
                ]

            }
        }
    }
</script>

<style scoped>

</style>