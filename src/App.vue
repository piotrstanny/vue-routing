<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-xs-12 col-sm-8">
                <h1>Routing</h1>
                <hr>
                <Header/>
                <router-view></router-view>
            </div>
        </div>
    </div>
</template>

<script>
import Header from './Header.vue'
    export default {
        components: {
            Header
        }
    }
</script>

<style>
.container {
    margin-top: 50px;
}
</style>
