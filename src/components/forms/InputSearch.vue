<template>
    <div class="search-container">
        <input
            class="input-search"
            type="text"
            placeholder="Search Employee..."
            name=""
            id=""
        />

        <i class="fa-solid fa-magnifying-glass search-icon"></i>
    </div>
</template>

<style lang="scss">
@import "@/scss/abstracts/_variables.scss";

.search-container {
    display: block;
    color: $color-light-gray;
    .input-search {
        width: 20rem;
        height: 3.6rem;
        background-color: transparent;
        border-radius: 0.4rem;
        border: 0.1rem solid $color-light-gray;
        font-size: $default-font-size;
        padding: 0 3.5rem 0 1rem;
        outline: none;

        &::-webkit-input-placeholder {
            color: $color-light-gray;
        }

        &:hover,
        &:focus {
            color: $color-cyan;
            border: 0.1rem solid $color-cyan;

            &::-webkit-input-placeholder {
                color: $color-cyan;
            }
        }
    }

    .search-icon {
        color: inherit;
        font-size: $default-font-size;
        position: relative;
        right: 3rem;
    }

    &:hover,
    &:focus-within {
        color: $color-cyan;

        &::-webkit-input-placeholder {
            color: $color-cyan;
        }
    }
}
</style>
