<template>
    <div>
        <section class="hero is-link">
            <div class="hero-body">
                <p class="title">
                    <i class="far fa-bell"></i>알람
                    <i class="fas fa-bicycle"></i>타슈
                </p>
                <p class="sub-title">
                    알람과 타슈의 연결고리
                </p>
            </div>
        </section>
        <section class="columns">
            <div class="column">
                <table class="table">
                    <table
                </table>
            </div>
            <div class="column"></div>
        </section>
    </div>
</template>
<script>
import { bicycle } from "~/assets/bicycle.json";

export default {
    data() {
        return {bicycle: bicycle.names};
    }
}
</script>
