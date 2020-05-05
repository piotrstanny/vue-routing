<template>
<div>
    <h3>Some User Details</h3>
    <p>User ID: {{ $route.params.id }}</p>
    <router-link tag="button" :to="{ name: 'userEdit', params: { id: $route.params.id } }">Edit</router-link>
</div>
</template>

<script>
export default {
    
    beforeRouteEnter(to, from, next) {
            console.log('Access allowed');
            next()
            // console.log('Access denied');
            // next(false)
        
    }
}
</script>