<template>
  <section class="container">
    <div class="indexWrap">
      <!-- <app-logo /> -->
      <ul>
        <li><nuxt-link to="/content">콘텐츠 화면</nuxt-link></li>
        <li><nuxt-link to="/form">입력 화면</nuxt-link></li>
        <li><nuxt-link to="/board/list">게시판</nuxt-link></li>
        <li><nuxt-link to="/calculator">계산기</nuxt-link></li>
        <li><nuxt-link to="/tab">탭</nuxt-link></li>
        <li><nuxt-link to="/table">테이블</nuxt-link></li>
        <li><nuxt-link to="/sync">학습 : Sync</nuxt-link></li>
        <li><nuxt-link to="/slots">학습 : Slot</nuxt-link></li>
        <li><nuxt-link to="/vevent">학습 : v-on</nuxt-link></li>
      </ul>
      <ul>
        <li><nuxt-link :to="{path:'/content', query:{id:1}}">콘텐츠 화면 파라미터1</nuxt-link></li>
        <li><nuxt-link :to="{path:'/content', query:{id:2}}">콘텐츠 화면 파라미터2</nuxt-link></li>
        <li><nuxt-link :to="{path:'/content', query:{id:3}}">콘텐츠 화면 파라미터3</nuxt-link></li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.container{margin:0 auto;width:800px;flex-direction: column;}
.indexWrap{}
.indexWrap ul{margin:15px 0;}
.indexWrap ul li{margin:5px 0;}
a{display:block;color:#000;text-decoration:none;}
a,button,input[type='button'],input[type='submit']{cursor:pointer;}
ul{display:block;list-style:none;margin:0;padding:0;}
ul > li{display:block;list-style:none;margin:0;padding:0;}
</style>
