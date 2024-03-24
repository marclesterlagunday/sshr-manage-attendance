<script setup>
import MenuItem from "@/components/nav/MenuItem.vue";
</script>

<template>
    <ul class="nav__menu">
        <MenuItem
            v-for="menu in menus"
            :key="menu.title"
            :title="menu.title"
            :link="menu.link"
            :sub="menu.sub"
        />
    </ul>
</template>

<script>
export default {
    data() {
        return {
            menus: [
                {
                    title: "My Requests",
                    link: "#",
                    sub: [],
                },
                {
                    title: "My Team",
                    link: "#",
                    sub: [],
                },
                {
                    title: "Company",
                    link: "#",
                    sub: [],
                },
                {
                    title: "Administration Tools",
                    link: "#",
                    sub: [],
                },
                {
                    title: "Maintenance",
                    link: "#",
                    sub: [],
                },
            ],
        };
    },
};
</script>

<style lang="scss">
.nav__menu {
    padding-right: 1rem;
}
</style>
