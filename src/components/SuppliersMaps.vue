<template>
    <div class="my-5">
        <gmap-map :center="{lat:10, lng: 10}" :zoom="7" style="width: 100%; height: 300px;">
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
</template>

<script>
    export default {
        name: "SuppliersMaps.vue",
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