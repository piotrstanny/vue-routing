<template>

    <ul class="nav justify-content-center navbar-dark bg-dark">
        <li class="nav-item">
            <router-link class="nav-link" to="/"><a>Home</a></router-link>
        </li>
        <li class="nav-item">
            <router-link class="nav-link" to="/user"><a>User</a></router-link>
        </li>
    </ul>

</template>

<style scoped>
.nav {
    margin-bottom: 30px
}
.nav-link {
    color: rgb(168, 168, 168)
}
.nav-link:hover {
    color: white
}
</style>
