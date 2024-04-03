<template>
    <Header />
    <Aside />
    <main class="main">
        <div class="main__header">
            <span>Date Range</span>
        </div>
    </main>
</template>

<script setup>
import Header from "@/components/layouts/Header.vue";
import Aside from "./components/layouts/Aside.vue";
</script>

<style lang="scss">
.main {
    float: right;
    &__header {
        display: flex;
        align-items: center;
    }
}
</style>
