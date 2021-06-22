<template>
  <div>
    <section class="hero is-primary">
      <div class="hero-body">
        <p class="title">
            <i class="far fa-newspaper"></i> 새로운 사실, 뉴스
        </p><br>
        <p class="subtitle">
          바쁘더라도 시사는 알고 살자<br>
          코로나도 알고 살자<br>
        </p>
      </div>
    </section>
    <br>
    <section class="hero is-success is-middle">
        네이버 뉴스, 다음 뉴스, 카카오 뉴스 등 유수의 뉴스들과 코로나 현황 파악하자.
    </section>
    <br>
    <section class="columns">
            <div class="column1">
                <table class="table is-striped is-hovable is-fullwidth">
                    <thead>
                        <th>사이트</th>
                        <th>이미지 클릭시 이동</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>네이버 뉴스</td>
                            <td><figure class="image is-128x128"> 
                                    <a href="https://news.naver.com/">
                                    <img src= "http://www.econovill.com/news/photo/201907/368292_267336_3425.jpg">
                                    </a>
                                </figure></td>
                        </tr>
                        <tr>
                            <td>다음 뉴스</td>
                            <td><figure class="image is-128x128">
                                <a href="https://news.daum.net/">
                            <img src= "https://postfiles.pstatic.net/20131028_148/sdkcool_13829445132533vlYi_JPEG/2013-10-28_161258.jpg?type=w2">
                            </a>
                            </figure></td>
                        </tr>
                        <tr>
                            <td>코로나 상황</td>
                            <td><figure class="image is-128x128">
                                <a href="http://ncov.mohw.go.kr/">
                            <img src= "http://www.efnews.co.kr/news/photo/202102/88976_63359_3454.jpg">
                            </a>
                            </figure></td>
                        </tr>
                        <tr>
                            <td>대전 코로나</td>
                            <td><figure class="image is-128x128">
                                <a href="http://corona.daejeon.go.kr/index.do/">
                            <img src="~assets/daejeon.png" alt="">
                            </a>
                            </figure></td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="column2">
                <table class="table is-striped is-hovable is-fullwidth">
                    <thead>
                        <th>사이트</th>
                        <th>이미지 클릭시 이동</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>네이버 뉴스</td>
                            <td><figure class="image is-128x128"> 
                                    <a href="https://news.naver.com/">
                                    <img src= "http://www.econovill.com/news/photo/201907/368292_267336_3425.jpg">
                                    </a>
                                </figure></td>
                        </tr>
                        <tr>
                            <td>다음 뉴스</td>
                            <td><figure class="image is-128x128">
                                <a href="https://news.daum.net/">
                            <img src= "https://postfiles.pstatic.net/20131028_148/sdkcool_13829445132533vlYi_JPEG/2013-10-28_161258.jpg?type=w2">
                            </a>
                            </figure></td>
                        </tr>
                        <tr>
                            <td>코로나 상황</td>
                            <td><figure class="image is-128x128">
                                <a href="http://ncov.mohw.go.kr/">
                            <img src= "http://www.efnews.co.kr/news/photo/202102/88976_63359_3454.jpg">
                            </a>
                            </figure></td>
                        </tr>
                        <tr>
                            <td>대전 코로나</td>
                            <td><figure class="image is-128x128">
                                <a href="https://www.daejeon.go.kr/corona19/">
                            <img src="~assets/daejeon.png" alt="">
                            </a>
                            </figure></td>
                        </tr>
                    </tbody>
                </table>
            </div>
    </section>
  </div>
</template>

<script>
    import axios from 'axios';
    export default{
        async asyncData(){
            const goodcoffee = await axios.get("https://raw.githubusercontent.com/wnshckdn/katerwnsgh_1/main/assets/coffee.json");
        
            return {
              tablecoffeeName: goodcoffee.data.Name,
              tablecoffeefrom: goodcoffee.data.from,
              tablecoffeeTaste: goodcoffee.data.Taste
            };
        }
    }
</script>