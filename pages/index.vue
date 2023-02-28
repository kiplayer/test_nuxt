<template>
  <section class="container">
    <div>
      <!-- <app-logo /> -->

      <nuxt-link to="/content">[콘텐츠 화면]</nuxt-link>
      <nuxt-link to="/form">[입력 화면]</nuxt-link>
      
      <nuxt-link :to="{path:'content', query:{id:1}}">[콘텐츠 화면 파라미터1]</nuxt-link>
      <nuxt-link :to="{path:'content', query:{id:2}}">[콘텐츠 화면 파라미터2]</nuxt-link>
      <nuxt-link :to="{path:'content', query:{id:3}}">[콘텐츠 화면 파라미터3]</nuxt-link>
    </div>
  </section>
</template>

<script>
import AppLogo from "~/components/AppLogo.vue";

export default {
  components: {
    AppLogo,
  },
};
</script>

<style>
.container{margin:0 auto;width:800px;flex-direction: column;}
a{display:block;}
/* .container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} */
</style>
