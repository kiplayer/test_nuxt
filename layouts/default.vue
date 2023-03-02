<template>
  <div id="wrap">
    <div id="header">
      <nuxt-link class="topLogo" to="/"><h1>Header</h1></nuxt-link>
      <a class="btn_back" @click="goBack">[뒤로가기]</a>
    </div>
    <div id="container">
      <nuxt/>
    </div>
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
html, body{margin:0;padding:0;}
#wrap{margin:0 auto;max-width:1200px;}
#header{position:relative;flex:1;height:80px;background-color:#eee;}
#header .topLogo{position:absolute;top:10px;left:0;}
#header .topLogo h1{margin:0;}
#header .btn_back{position:absolute;top:0;right:0;}
#container{padding:30px 0;min-height:600px;}
#footer{position:relative;flex:1;padding:10px 0;background-color:#eee;}
</style>

