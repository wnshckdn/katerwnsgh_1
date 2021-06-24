<template>
  <div>
    <nav class="breadcrumb">
        <ul>
          <li><nuxt-link to="/"><i class="fas fa-home"></i>&nbsp; 홈으로</nuxt-link></li>
          <li><nuxt-link to="/worldBicycle"><i class="fas fa-bicycle"></i>&nbsp; 자전거 브랜드</nuxt-link></li>
          <li><nuxt-link to="/goodcoffee"><i class="fas fa-coffee"></i>&nbsp; 활력소 커피</nuxt-link></li>
          <li><nuxt-link to="/tashu"><i class="fas fa-bicycle"></i>&nbsp; 아침의 조력자, 타슈</nuxt-link></li>
          <li><nuxt-link to="/bustime"><i class="fas fa-bus"></i>&nbsp; 출근길 도우미, 버스</nuxt-link></li>
          <li><nuxt-link to="/news"><i class="far fa-newspaper"></i>&nbsp; 좋은 소식통, 뉴스</nuxt-link></li>
        </ul>
    </nav>
    <nuxt/>
    <footer class="footer">
      <div class="content has-text-centered">
        <i class="fas fa-copyright"></i> 2020-2021, 모든 저작권은 <strong>개발자 김준호</strong>에 있습니다
      </div>
    </footer>
  </div>
</template>

