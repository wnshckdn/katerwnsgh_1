<template>
  <div>
    <nav class="breadcrumb">
        <ul>
          <li><nuxt-link to="/"><i class="fas fa-home"></i>&nbsp; 홈으로</nuxt-link></li>
          <li><nuxt-link to="/worldBicycle"><i class="fas fa-bicycle"></i>&nbsp; 자전거 브랜드</nuxt-link></li>
          <li><nuxt-link to="/goodcoffee"><i class="fas fa-coffee"></i>&nbsp; 상쾌한 커피</nuxt-link></li>
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

