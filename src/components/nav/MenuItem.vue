<template>
    <li class="nav__menu-item">
        <a :href="link">
            {{ title }}
            <i class="fa-solid fa-caret-down"></i>
        </a>
    </li>
</template>

<script>
export default {
    props: {
        title: { required: true, type: String },
        link: { default: "#", type: String },
        sub: { required: false, type: Object },
    },
};
</script>

<style lang="scss">
@import "@/scss/abstracts/_variables.scss";

.nav__menu-item {
    display: table;
    float: left;
    list-style: none;
    padding: 0.8rem;

    a {
        display: table-cell;
        vertical-align: middle;
        color: $color-light-gray;
        text-decoration: none;
        height: 3rem;
        font-size: $default-font-size;

        &:hover {
            color: $color-cyan;
        }
    }
}
</style>
