<template>
    <div>
        <div class="py-5">
            <gmap-map :center="{lat:10, lng: 10}" :zoom="7" style="width: 100%; height: 600px; margin-top: 20px">
                <GmapMarker
                        :key="index"
                        v-for="(m, index) in markers"
                        :position="m.position"
                        :clickable="true"
                        :draggable="true"
                        @click="center=m.position"
                />
            </gmap-map>
        </div>
    </div>
</template>

<script>
    import Suppliers from './SuppliersListe'
    export default {
        name: "SuppliersMaps.vue",
        components: {Suppliers},
        data (){
            return {
                markers: [
                    {
                        id: 1,
                        position: {
                            lat: 10,
                            lng: 10
                        }
                    },
                    {
                        id: 2,
                        position: {
                            lat: 11,
                            lng: 9.6
                        }
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>