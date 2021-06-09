<template>
    <div>
        <section class="hero is-success">
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
        <section class="hero is-success">
            <div class="hero-body">
                <p class="title">
                    <i class="fas fa-bicycle"></i> 타슈
                </p>
                <p class="sub-title">
                    없으면 타슈를 탑시다
                </p>
            </div>
        </section>
        
        <section class="columns">
            <div class="column">
                <article class="notification">
      <table class="table is-striped is-hovable is-fullwidth">
        <thead>
            <tr>
              <th>자전거 대여</th>
              <th>타슈 페이지</th>
            </tr>
        </thead>
        <tbody>
          <tr>
            <td>이용방법</td>
            <td><a href="https://www.tashu.or.kr/introduceAction.do?process=howtorent">페이지 이동</a></td>
          </tr>
          <tr>
            <td>실시간 현황</td>
            <td><a href="https://www.tashu.or.kr/status.do?process=userStatusView&left=2">페이지 이동</a></td>
          </tr>
          <tr>
            <td>대여소 정보</td>
            <td><a href="https://www.tashu.or.kr/userStationAction.do?process=stationTotalList">페이지 이동</a></td>
          </tr>
          <tr>
            <td>의무와 책임</td>
            <td><a href="https://www.tashu.or.kr/introduceAction.do?process=charges&left=1">페이지 이동</a></td>
          </tr>
        </tbody>
      </table>
      </article>
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
