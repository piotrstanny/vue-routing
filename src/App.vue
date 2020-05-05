<template>
    <div class="container-fluid">
        <div class="row justify-content-center">
            <div class="col-xs-12 col-sm-8">
                <h1>Routing</h1>
                <hr>
                <Header/>
                <transition name="slide" mode="out-in">
                    <router-view ></router-view>
                </transition>
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

/* Sliding animation */
.slide-enter-active {
    animation: slide-in .5s ease-out forwards;
    /* transition: opacity .4s; */
}
.slide-leave {

}
.slide-leave-active {
    animation: slide-out .2s ease-in forwards;
    transition: opacity .2s;
    opacity: 0;
}
@keyframes slide-in {
    from {
        transform: translateX(20px);
    }
    to {
        transform: translateX(0);
    }
}
@keyframes slide-out {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(-20px);
    }
}
</style>
