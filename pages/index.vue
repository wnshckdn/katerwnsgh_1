<template>
  <div>
    <section class="hero is-primary">
      <div class="hero-body">
        <p class="title">
            <i class="far fa-bell"></i> 현대인의 상쾌한 아침
        </p><br>
        <p class="subtitle">
          월요일은 밝게...<br><br>
          화요일은 활기차게..<br><br>
          수요일은 새롭게!<br><br>
          목요일은 기쁘게!!<br><br>
          금요일은 불타게!!!
        </p>
      </div>
    </section>
    <br>
    <div class="columns">
      <div class="column1">
          <article class="message-info">
            <div class="message-header">
              <p>알람, 하루의 상쾌함</p>
            </div>
            <div class="message-body">
              <div class="columns">
                <div class="column1">
                  <figure class="image is-128x128">
                <img src="https://previews.123rf.com/images/tmricons/tmricons1510/tmricons151000008/45799794-%EC%95%8C%EB%9E%8C-%EC%95%84%EC%9D%B4%EC%BD%98-.jpg">
                </figure>
                </div>
                <div class="column2">
                  <figure class="image is-128x128">
                  <img src="~assets/alarm.png" alt=""> 
                </figure>
                </div>
              </div>
              <br>
                Alarm은 불안, 공포 및 경보(음), 그리고 자명종을 의미하는 영단어이다.
한국에서는 '모닝콜'이라는 말을 자주 쓰고 있는데 이 단어의 어원은 영어가 아니라 재플리시인 モーニングコール이다. 참고로 모닝콜은 호텔 등에서 아침에 고객을 전화로 깨워준다는 것뿐 아니라, 아침에 타인이 전화를 걸어서 깨워준다는 의미도 포함한다. 재플리시라서 당연히 외국에선 통하지 않는다. 특히 영어권에서 morning call이라는 이야기를 아침에 호텔에서 하면 아침 회의로 착각할 수 있다. 전화로 깨워 주는 서비스를 원한다면 '웨이크 업 콜(wake-up call)'이라고 해야 한다.
                          <br>
      <section class="hero is-success is-middle">
        {{tablemorningname[0]}}
      </section>
        {{tablemorningdoing[0]}}
      <br>
      <section class="hero is-success is-middle">
        {{tablemorningname[1]}}
      </section>
        {{tablemorningdoing[1]}}
      <br>
      <section class="hero is-success is-middle">
        {{tablemorningname[2]}}
      </section>
        {{tablemorningdoing[2]}}
      <br>
      <section class="hero is-success is-middle">
        {{tablemorningname[3]}}
      </section>
        {{tablemorningdoing[3]}}
      <br>
      <section class="hero is-success is-middle">
        {{tablemorningname[4]}}
      </section>
        {{tablemorningdoing[4]}}
      <br>

      </div>
            
      </article>

      </div>
      </div>
  </div>
</template>
<script>
    import axios from 'axios';
    export default{
        async asyncData(){
            const morning = await axios.get("https://raw.githubusercontent.com/wnshckdn/katerwnsgh_1/main/assets/tashu.json");
        
            return {
              tablemorningname: morning.data.name,
              tablemorningdoing: morning.data.doing
            };
        }
    }
</script>