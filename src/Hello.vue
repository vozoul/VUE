<template>
    <div class="card">
        <h1>{{ message }}</h1>
        <h2>{{ person.firstName }} {{ person.lastName }}!</h2>
        <h2>{{ firstName }} {{ lastName }} de {{ from }}!</h2>
        <label>Firstname : <input type="text" v-model="person.firstName"></label>
        <label>Lastname : <input type="text" v-model="person.lastName"></label>
        <label>Message : <input type="text" v-model="message"></label>
    </div>
</template>

<script>
    export default {
        name: "Hello.vue",
        data() {
            return {
                person: {
                    firstName: "John",
                    lastName: "doe",
                    from: "Paris",
                },
                message: "Welcome",
            }
        },
        props: ['firstName', 'lastName', 'from', 'image'],
    }
</script>

<style scoped>
</style>