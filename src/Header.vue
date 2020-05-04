<template>

    <ul class="nav justify-content-center navbar-dark bg-dark">
        <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
        </li>
        <li class="nav-item">
            <router-link class="nav-link" to="/user">User</router-link>
        </li>
    </ul>

</template>

<style scoped>
.nav {
    margin-bottom: 30px;
}
.nav-link {
    color: rgb(158, 158, 158)
}
.nav-link:hover {
    color: white
}
</style>