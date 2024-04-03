<template>
    <aside class="aside">
        <!-- Header -->
        <div class="aside__header">
            <h3 class="aside__header-title">Manage Attendance</h3>
            <p class="aside__header-description">
                Attendance management is where you can generate, add, edit, and
                export the logs of the employees.
            </p>
        </div>

        <!-- Nav -->
        <div class="aside__nav">
            <button class="aside__nav-btn active" type="button">
                <i class="fa-regular fa-calendar-days"></i>&nbsp; Attendance
                Logs
            </button>
            <button class="aside__nav-btn" type="button">
                <i class="fa-solid fa-download"></i>&nbsp; Exported Files
            </button>
        </div>

        <!-- Filters -->
        <div class="filters">
            <div class="filters__date-range">
                <h3 class="filters__title">DATE RANGE</h3>
                <InputDate label="Date From" />
                <InputDate label="Date To" />
            </div>
            <div class="filters__options">
                <div class="filters__options-head">
                    <h3 class="filters__title">FILTERS</h3>
                    <a href="">Show All</a>
                </div>
                <div class="filters__items">
                    <div class="filters__items-selected">
                        <img src="/images/icons/buildings.png" alt="" />
                        <p>SPROUT SOLUTIONS</p>
                    </div>
                    <div class="filters__items-selected">
                        <img src="/images/icons/users.png" alt="" />
                        <p>ALL</p>
                    </div>
                    <div class="filters__items-selected">
                        <img src="/images/icons/map.png" alt="" />
                        <p>ALL</p>
                    </div>
                    <div class="filters__items-selected">
                        <img src="/images/icons/single-user.png" alt="" />
                        <p>ALL</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Action Buttons -->
        <div class="actions">
            <Btn type="button" primary>
                <i class="fa-solid fa-magnifying-glass"></i> Search
            </Btn>
            <Btn type="button" secondary>
                <i class="fa-solid fa-download"></i> Export
            </Btn>
        </div>
    </aside>
</template>

<script setup>
import InputDate from "@/components/forms/InputDate.vue";
import Btn from "@/components/Button.vue";
</script>

<style lang="scss">
.aside {
    width: 35.4rem;
    height: auto;
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
    border-bottom: 0.1rem solid #c3cdc9;

    &__title {
        font-size: 1.4rem;
        font-weight: 500;
        color: #3c5b51;
        line-height: 1.4rem;
        margin-bottom: 1.8rem;
        letter-spacing: 0.08rem;
    }

    &__options {
        &-head {
            display: flex;
            justify-content: space-between;
            align-items: center;

            a {
                margin-bottom: 1.8rem;
                text-decoration: none;
                color: #0f6eeb;
                font-weight: 500;
                font-size: 1.4rem;
            }
        }
    }

    &__items {
        &-selected {
            display: flex;
            align-items: center;
            margin-bottom: 0.5rem;
            p {
                font-size: 1.4rem;
                margin: 0;
            }
            img {
                height: 2rem;
                margin-right: 0.75rem;
            }
        }
    }
}

.actions {
    padding: 2.4rem;
}
</style>
