<template>
    <Header />
    <main class="main">
        <Aside />
        <div class="container">
            <div class="main__header">
                <p class="date-range">
                    <i class="fa-solid fa-calendar primary-icon"></i>
                    &nbsp; Date Range
                </p>
                <p class="date-range"></p>
            </div>

            <div class="table">
                <div class="table__content">
                    <div class="no-results">
                        <img src="/images/no-payslip.png" alt="no-payslip" />
                        <h3>No attendance logs to show</h3>
                        <p>Get started by searching for the logs</p>
                    </div>
                </div>
                <div class="table__footer">
                    <div class="items-per-page">
                        Items per page &nbsp;
                        <select name="items" id="items">
                            <option value="10">10</option>
                            <option value="20">20</option>
                            <option value="30">30</option>
                            <option value="40">40</option>
                        </select>
                    </div>
                    <div class="page">Page 1 of 1</div>
                    <div class="showing">Showing 0 of 0</div>
                </div>
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
    grid-template-columns: auto 1fr;

    .container {
        width: 100%;
        padding: 3rem 2.4rem 8rem 2.4rem;
    }

    &__header {
        width: 100%;
        display: flex;
        justify-content: space-between;

        .date-range {
            font-size: 1.6rem;
            font-weight: 500;
            color: #00291b;
            margin-bottom: 2rem;
        }
    }

    .table {
        border: 0.1rem solid #c3cdc9;
        border-radius: 0.4rem;
        height: 100%;
        width: 100%;
        margin-bottom: 2.4rem;
        display: grid;
        grid-template-rows: auto 6.4rem;

        &__content {
            display: flex;
            justify-content: center;
            align-items: center;

            .no-results {
                text-align: center;
                h3 {
                    font-size: 2.4rem;
                    font-weight: 500;
                    margin-bottom: 0rem;
                }
                p {
                    font-size: 1.6rem;
                    font-weight: 400;
                }
            }
        }

        &__footer {
            border-top: 0.1rem solid #c3cdc9;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.6rem;
            color: #3c5b51;
            font-size: 1.4rem;
            font-weight: 400;
        }
    }

    .primary-icon {
        color: #17ad49;
    }
}
</style>
