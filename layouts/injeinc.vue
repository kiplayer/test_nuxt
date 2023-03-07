<template>
  <div id="wrap">
    <div id="header">
      <div class="inner">
        <nuxt-link to="/"><h1><img src="/images/main/Logo.png" alt=""></h1></nuxt-link>
        <Gnb />
      </div>
    </div>
    <div id="container">
      <nuxt/>
    </div>
    <div id="footer">
      <div class="inner">
        <div class="logo"><nuxt-link to="/"><img src="/images/main/f_logo.png" alt=""></nuxt-link></div>
        <div class="address">
          본사 : 서울시 구로구 디지털로 33길 12, 1301호(구로동, 우림이비즈센터2차) / 대표 전화 : 070-4609-6333<br />
          대전지사 : 대전시 서구 둔산대로 117번길 66, 909호( 만년동 , 골드벤처타워 )
        </div>
        <div class="right">
          <ul class="nav">
            <li><nuxt-link to="/">개인정보처리방침</nuxt-link></li>
            <li><nuxt-link to="/">Contact us</nuxt-link></li>
          </ul>
          <div class="copyright">
            Copyright ⓒ Injeinc Co., Ltd. All Rights Reserved.
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Gnb from '../components/Gnb';
export default {
  components: {
    Gnb,
  }
}
</script>

<style>
html, body{margin:0;padding:0;}
h1,h2,h3,h4,h5,h6{margin:0;padding:0;}
a{color:#000;text-decoration:none;}
a,button,input[type='submit'],input[type='button']{cursor:pointer;}
ul,ol,li{margin:0;padding:0;list-style:none;}

.inner{position:relative;margin:0 auto;width:1180px;}
#header{position:relative;box-shadow:0 0 5px rgb(0 0 0 / 15%);z-index:99;}
#header .inner{display:flex;flex-direction:row;justify-content:center;}
#header h1{display:flex;height:85px;}
#header h1 img{height:50px;align-self:center;}
#header .btn_back{position:absolute;top:0;right:0;margin:10px;}
#header:before{display:block;content:'';position:absolute;left:0;right:0;top:85px;height:0;background:#fff;transition-duration:0.3s;box-shadow:0 0 5px rgb(0 0 0 / 15%);}
#header.subOpened:before{height:80px;}
#container{padding:30px 0;min-height:600px;}
#footer{padding:40px 0;color:#fff;line-height:25px;background-color:#000000;}
#footer a{color:#fff;}
#footer .inner{display:flex;flex-direction:row;}
#footer .logo{margin-right:50px;}
#footer .address{font-size:14px;}
#footer .right{float:right;}
#footer .copyright{color:#666;clear:both;}
#footer .nav{display:block;float:right;overflow:hidden;margin-right:-10px;}
#footer .nav li{display:block;position:relative;float:left;padding:0 10px;}
#footer .nav li:after{display:block;content:'';position:absolute;top:50%;right:-1px;margin-top:-5px;height:10px;border-right:1px #fff solid;}
</style>

