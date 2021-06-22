<template>
  <div>
    <section class="hero is-small is-primary">
      <div class="hero-body">
        <p class="title">
            <i class="fas fa-bicycle"></i> 현대인의 상쾌한 아침
        </p>
        <p class="subtitle">
          늦지않게 일하러가자
        </p>
      </div>
    </section>
    <br>
      <div class="column1">
          <article class="message-info">

            <div class="message-header">
              <p>타슈, 활기찬 아침을 책임진다</p>
            </div>
            <div class="message-body">
              <div class="columns">
                <div class="column1">
                  <figure class="image is-128x128">
                
                <img src="https://www.daejeon.go.kr/images/bike/contents/tasu.png">
                </figure>
                </div>
                <div class="column2">
                  <figure class="image is-128x128">
                &nbsp;<img src="~assets/tashu.jpg" alt="">
                </figure>
                </div>
              </div>
              <br>
               타슈는 2008년 부터 대전광역시에서 운영되고 있는 무인 대여 공공자전거 서비스다. 둔산신도시 및 도안신도시를 중심으로 주변지역에 집중적으로 비치되어 있으며, 주요 관공서나 지하철역 근처에도 비치되어 있다. 현재 중구와 대덕구, 동구의 대여소가 크게 확충되어 대부분의 대전광역시 전역으로 타슈가 확장되어 음영지역을 제외하고 대전 도심의 대부분에서 타슈를 이용할 수 있다. 또한 정부세종청사에도 대여소가 하나 있었지만 현재는 어울링 대여소로 변경되어서 운영 중에 있다.
              </div>
      </article>
      
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
      </div>
  </div>
</template>

<script>
    import axios from 'axios';
    export default{
        async asyncData(){
            const tashu = await axios.get("https://raw.githubusercontent.com/wnshckdn/katerwnsgh_1/main/assets/coffee.json");
        
            console.log(goodcoffee)
            return {
              tabletashuName: tashu.data.name,
              tabletashuaddress: tashu.data.address
            };
        }
    }
</script>