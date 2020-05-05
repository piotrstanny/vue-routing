<template>
<div>
    <h3>Some User Details</h3>
    <p>User ID: {{ $route.params.id }}</p>
    <router-link tag="button" :to="'/user/' + $route.params.id + '/edit'">Edit</router-link>
</div>
</template>