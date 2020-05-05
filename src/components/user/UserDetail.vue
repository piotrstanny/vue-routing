<template>
<div>
    <h3>Some User Details</h3>
    <p>User ID: {{ $route.params.id }}</p>
    <router-link tag="button" :to="{ name: 'userEdit', params: { id: $route.params.id } }">Edit</router-link>
</div>
</template>

<script>
export default {
    data() {
        return {
            permission: true
        }
    },
    beforeRouteEnter(to, from, next) {
        if (true) {
            console.log('Access allowed');
            next()
        } else {
            console.log('Access denied');
            next(false)
        }
    }
}
</script>