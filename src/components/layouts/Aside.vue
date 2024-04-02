<template>
    <aside class="aside">
        <div class="aside__header">
            <h3 class="aside__header-title">Manage Attendance</h3>
            <p class="aside__header-description">
                Attendance management is where you can generate, add, edit, and
                export the logs of the employees.
            </p>
        </div>
        <div class="aside__nav">
            <button class="aside__nav-btn active" type="button">
                <i class="fa-regular fa-calendar-days"></i>&nbsp; Attendance
                Logs
            </button>
            <button class="aside__nav-btn" type="button">
                <i class="fa-solid fa-download"></i>&nbsp; Exported Files
            </button>
        </div>

        <div class="filters">
            <div class="filters__date-range">
                <h3 class="filters__title">DATE RANGE</h3>
                <InputDate label="Date From" />
                <InputDate label="Date To" />
            </div>
            <div class="filters__options">
                <h3 class="filters__title">FILTERS</h3>
            </div>
        </div>
    </aside>
</template>

<script setup>
import InputDate from "@/components/forms/InputDate.vue";
</script>

<style lang="scss">
.aside {
    width: 35.4rem;
    height: calc(100vh - 7.6rem);
    border-right: 0.1rem solid #879a94;

    &__header {
        padding: 2.4rem 3.2rem;
        color: #00291b;
        &-title {
            font-size: 2.4rem;
            font-weight: 500;
            line-height: 3.2rem;
            margin-bottom: 0.8rem;
        }
        &-description {
            font-size: 1.4rem;
            line-height: 2.4rem;
            font-weight: 400;
        }
    }

    &__nav {
        display: flex;
        flex-direction: column;
        align-items: center;
        border-bottom: 0.1rem solid #c3cdc9;
        height: 12rem;
        &-btn {
            width: 30.6rem;
            height: 4.8rem;
            padding: 1.6rem;
            border-radius: 0.4rem;
            display: block;
            border: none;
            background-color: transparent;
            cursor: pointer;
            color: #5a756b;
            font-size: 1.6rem;
            font-weight: 500;
            text-align: start;
            line-height: 1.6rem;

            &:hover {
                background-color: #e6ffee;
                color: #2d4f43;
            }

            &.active {
                background-color: #e6ffee;
                color: #2d4f43;
            }
        }
    }
}

.filters {
    padding: 2.4rem;

    &__title {
        font-size: 1.4rem;
        font-weight: 500;
        color: #3c5b51;
        line-height: 1.4rem;
        margin-bottom: 1.8rem;
        letter-spacing: 0.08rem;
    }
}
</style>
