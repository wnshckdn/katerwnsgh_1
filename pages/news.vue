<template>
  <div>
    <section class="hero is-small is-danger">
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
    <section class="hero is-small is-success">
        &nbsp;&nbsp;네이버 뉴스, 다음 뉴스, 여러 언론사의 뉴스들과 코로나 현황 파악하자.
    </section>
    <br>
        <table class="table is-striped is-hovable is-fullwidth">
            <thead>
                <th>사이트</th>
                <th>이미지 클릭시 이동</th>
                <th>뉴스 사이트</th>
                <th>이미지 클릭시 이동</th>
            </thead>
            <tbody>
                <tr>
                    <td>{{tablenewsname[0]}}</td>
                    <td><figure class="image is-128x128"> 
                            <a href="https://news.naver.com/">
                            <img src= "http://www.econovill.com/news/photo/201907/368292_267336_3425.jpg">
                            </a>
                        </figure></td>
                        <td>{{tablenewsname[4]}}</td>
                    <td><figure class="image is-128x128"> 
                            <a href="https://www.ytn.co.kr/">
                    <img src="~assets/ytn.PNG" alt="">
                            </a>
                        </figure></td>
                </tr>
                <tr>
                    <td>{{tablenewsname[1]}}</td>
                    <td><figure class="image is-128x128">
                        <a href="https://news.daum.net/">
                    <img src= "http://www.urbanbrush.net/web/wp-content/uploads/edd/2017/09/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7-2017-09-24-%EC%98%A4%ED%9B%84-7.09.57-1560x1098.png">
                    </a>
                    </figure></td>
                    <td>{{tablenewsname[5]}}</td>
                    <td><figure class="image is-128x128">
                        <a href="https://www.mbn.co.kr/">
                    <img src="~assets/mbn.PNG" alt="">
                    </a>
                    </figure></td>
                </tr>
                <tr>
                    <td>{{tablenewsname[2]}}</td>
                    <td><figure class="image is-128x128">
                        <a href="http://ncov.mohw.go.kr/">
                    <img src= "http://www.efnews.co.kr/news/photo/202102/88976_63359_3454.jpg">
                    </a>
                    </figure></td>
                    <td>{{tablenewsname[6]}}</td>
                    <td><figure class="image is-128x128">
                        <a href="https://www.yna.co.kr/index?site=header_logo">
                    <img src="~assets/yhn.PNG" alt=""></a>
                    </figure></td>
                </tr>
                <tr>
                    <td>{{tablenewsname[3]}}</td>
                    <td><figure class="image is-128x128">
                        <a href="http://corona.daejeon.go.kr/index.do/">
                    <img src="~assets/daejeon.PNG" alt="">
                    </a>
                    </figure></td>
                    <td>{{tablenewsname[7]}}</td>
                    <td><figure class="image is-128x128">
                        <a href="https://news.kbs.co.kr/common/main.html?ref=pLogo">
                    <img src="~assets/kbs.PNG" alt=""> </a>
                    </figure></td>
                </tr>
            </tbody>
        </table>
        <div class="content">
            <span class="tag is-danger"><a href="https://github.com/wnshckdn/katerwnsgh_1">출처</a></span><span>&nbsp;myself</span>
            </div>
  </div>
</template>

<script>
    import axios from 'axios';
    export default{
        async asyncData(){
            const newsname = await axios.get("https://raw.githubusercontent.com/wnshckdn/katerwnsgh_1/main/assets/newsname.json");
        
            return {
              tablenewsname: newsname.data.name
            };
        }
    }
</script>