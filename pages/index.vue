<template>
  <section class="container">
    <div>
      <!-- <app-logo /> -->

      <nuxt-link to="/content">[콘텐츠 화면]</nuxt-link>
      <nuxt-link to="/form">[입력 화면]</nuxt-link>
      <nuxt-link to="/board/list">[게시판 - 목록 화면]</nuxt-link>
      
      <nuxt-link :to="{path:'/content', query:{id:1}}">[콘텐츠 화면 파라미터1]</nuxt-link>
      <nuxt-link :to="{path:'/content', query:{id:2}}">[콘텐츠 화면 파라미터2]</nuxt-link>
      <nuxt-link :to="{path:'/content', query:{id:3}}">[콘텐츠 화면 파라미터3]</nuxt-link>
    </div>
  </section>
</template>

<style>
.container{margin:0 auto;width:800px;flex-direction: column;}
a{display:block;color:#000;text-decoration:none;}
a,button,input[type='button'],input[type='submit']{cursor:pointer;}
/* .container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} */
ul{display:block;list-style:none;margin:0;padding:0;}
ul > li{display:block;list-style:none;margin:0;padding:0;}
</style>
