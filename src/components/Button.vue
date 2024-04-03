<template>
    <button v-bind="$attrs" :class="getClass()" class="btn">
        <slot />
    </button>
</template>

<script>
export default {
    methods: {
        getClass() {
            return {
                primary: this.$attrs["primary"] != null,
                secondary: this.$attrs["secondary"] != null,
            };
        },
    },
};
</script>

<style lang="scss">
.btn {
    width: 100%;
    padding: 1.6rem;
    font-weight: 500;
    font-size: 1.6rem;
    cursor: pointer;
    border-radius: 0.4rem;
    outline: none;
    margin-bottom: 0.8rem;
}

.primary {
    background-color: #17ad49;
    color: #ffffff;
    border: none;
}

.secondary {
    background-color: #ffffff;
    color: #17ad49;
    border: 0.1rem solid #17ad49;
}
</style>
