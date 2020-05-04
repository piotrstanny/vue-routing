<template>
<div>
    <h1>The User Page</h1>
    <hr>
    <p>Id: {{ id }}</p>
    <button @click="navigateHome">Go to Home</button>
</div>

</template>

<script>
export default {
    data() {
        return {
            id: this.$route.params.id
        }
    },
    watch: {
        '$route'(to) {
            this.id = to.params.id
        }
    },
    methods: {
        navigateHome() {
            this.$router.push({path: '/'})
        }
    }
}
</script>