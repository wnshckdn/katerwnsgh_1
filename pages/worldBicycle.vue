<template>
    <div>
        <section class="hero is-small is-success">
            <div class="hero-body">
                <p class="title">
                    <i class="fas fa-bicycle"></i> 자전거 브랜드
                </p>
                <p class="sub-title">
                    인지도 있고 좋은 자전거 브랜드
                </p>
            </div>
        </section>
        <section class="columns">
            <div class="column">
                <section class="columns">
                    <div class="column">
                        <figure class="image is-full-width">
                            <img src= "https://mblogthumb-phinf.pstatic.net/20160511_33/odbikem_1462958909611s6MAM_JPEG/p5pb13343822.jpg?type=w800">
                        </figure>
                    </div>
                    <div class="column">
                        <figure class="image is-256x300">
                            <img src= "https://www.altonsports.com/prdimg/get/SPEEDER-lite-21-1_1060X600.png">
                        </figure>
                    </div>
                    <div class="column">
                        <figure class="image is-full-width">
                            <img src= "https://www.bikeinn.com/f/13752/137525039/cinelli-superstar-disc-ultegra-2020-road-bike.jpg">
                        </figure>
                    </div>
                    <div class="column">
                        <figure class="image is-256x256">
                            <img src= "https://images.giant-bicycles.com/b_white,c_pad,h_650,q_80/tnxykjf4dszs1ebnv9s4/MY20ATX227-5_ColorA.jpg">
                        </figure>
                    </div>
                </section>
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
            <span class="tag is-danger"><a href="https://github.com/wnshckdn/katerwnsgh_1">출처</a></span><span>&nbsp;myself</span>
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
