<template>
    <Header />
    <main class="main">
        <Aside />
        <div class="container">
            <div class="main__header">
                <!-- <p class="date-range">Date Range</p>
                <p class="date-range">Date Range</p> -->
            </div>
        </div>
    </main>
</template>

<script setup>
import Header from "@/components/layouts/Header.vue";
import Aside from "./components/layouts/Aside.vue";
</script>

<style lang="scss">
.main {
    display: grid;
    grid-template-columns: 1fr auto;

    &__header {
        width: 100%;
        display: flex;
        justify-content: start;
    }
}
</style>
