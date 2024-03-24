<template>
    <header class="header">
        <nav class="nav">
            <img
                class="nav__logo"
                src="/images/main-logo.png"
                alt="main-logo"
            />

            <div class="nav__actions">
                <Menu />
                <InputSearch />

                <div class="user">
                    <div class="user__avatar"></div>
                    <AdminMenu title="Admin" />
                </div>
            </div>
        </nav>
    </header>
</template>

<script setup>
import Menu from "@/components/nav/Menu.vue";
import InputSearch from "@/components/forms/InputSearch.vue";
import AdminMenu from "@/components/nav/MenuItem.vue";
</script>

<style lang="scss">
@import "@/scss/abstracts/_variables.scss";

.header {
    height: 7.6rem;
    background-color: #333333;

    .nav {
        width: 100%;
        height: 100%;
        padding: 1.8rem 2rem 1.8rem 3rem;
        position: relative;

        &__logo {
            width: 17.1rem;
            height: 3.8rem;
        }

        &__actions {
            float: right;
            display: flex;
            align-items: center;

            .user {
                display: inline-flex;
                align-items: center;
                &__avatar {
                    height: 30px;
                    width: 30px;
                    background-color: #c4c4c4;
                    border-radius: 50%;
                }
            }
        }
    }
}
</style>
