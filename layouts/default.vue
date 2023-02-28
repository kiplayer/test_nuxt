<template>
  <div id="wrap">
    <div id="header">
      <nuxt-link to="/"><h1>Header</h1></nuxt-link>
      <a class="btn_back" @click="goBack">[뒤로가기]</a>
    </div>
    <nuxt/>
    <div id="footer">
      Footer
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    goBack() {
      this.$router.go(-1)
    }
  }
}
</script>

<style>
#wrap{margin:0 auto;max-width:1200px;}
#header{position:relative;flex:1;}
#header .btn_back{position:absolute;top:0;right:0;}
</style>

