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
                            <th>순번</th>
                            <th>자전거 브랜드</th>
                            <th>브랜드 국적</th>
                            <th>주요 상품</th>
                        </tr>
                    </thead>
                    <tbody>
                        <template v-for = "pos in tableBicycle.length">
                            <tr :key="pos">
                                <td> 
                                    {{ pos }} 
                                </td>
                                <td>
                                    {{tableBicycle [pos - 1]}}
                                </td>
                                <td>
                                    {{tableBicycleFrom [pos - 1]}}
                                </td>
                                <td>
                                    {{tableBicycleProduct [pos - 1]}}
                                </td>
                            </tr>
                        </template>
                    </tbody>
                </table>
            <div class="content">
            <span class="tag is-danger">출처</span><span>&nbsp;myself</span>
            </div>
            </div>
        </section>
    </div>
</template>
<script>
import  worldBicycle  from "@/assets/bicycle.json";

export default {
    data() {
        return {
            tableBicycle: worldBicycle.names,
            tableBicycleFrom: worldBicycle.from,
            tableBicycleProduct: worldBicycle.Product
        }
    }
}
</script>
