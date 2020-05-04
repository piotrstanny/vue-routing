<template>
<div>
    <h1>The User Page</h1>
    <hr>
    <button @click="navigateHome">Go to Home</button>
</div>

</template>

<script>
export default {
    methods: {
        navigateHome() {
            this.$router.push({path: '/'})
        }
    }
}
</script>