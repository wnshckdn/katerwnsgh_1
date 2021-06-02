<template>
  <div>
    <nav class="breadcrumb">
        <ul>
          <li><nuxt-link to><i class="fas fa-home"></i>&nbsp;홈으로</nuxt-link></li>
          <li><nuxt-link to="/alarm"><i class="fas fa-file-signature"></i>&nbsp;알람</nuxt-link></li>
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

