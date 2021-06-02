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
                <table class="table is-striped is-hovable is-fullwidth">
                    <thead>
                        <tr>
                            <th>자전거 브랜드</th>
                        </tr>
                    </thead>
                    <tbody>
                        <template v-for="pos in tableBicycle.length">
                            <tr :key="pos">
                                <td> {{ pos }} </td>
                                <td>{{tableBicycle[pos - 1]}}</td>
                            </tr>
                        </template>
                    </tbody>
                </table>
            </div>
            <div class="column"></div>
            <div class="content">
            <span class="tag is-danger">출처</span><span>myself</span>
            </div>
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
