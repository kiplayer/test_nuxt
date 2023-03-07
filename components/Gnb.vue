<template>
  <div id="gnb">
    <!-- <h2 class="logo"><a href="/">메인로고</a></h2> -->
    <ul> 
      <li>
        <a href="/">Service</a>
        <ul>
          <li><a href="/">Cloud 설계ㆍ구축 </a></li> 
          <li><a href="/">솔루션/커스터마이징</a></li> 
          <li><a href="/">컨설팅/매니지드 서비스</a></li> 
          <li><a href="/">SI/SM</a></li>
        </ul>
      </li>
      <li>
        <a href="/">Solutions</a>
        <ul>
          <li><a href="/">CONE-Plus(CMP)</a></li> 
          <li><a href="/">CONE-PaaS</a></li> 
          <li><a href="/">CONE-IaaS</a></li> 	
          <li><a href="/">CONE-DevOps</a></li>
          <li><a href="/">CONE-IDE</a></li>
        </ul>
      </li>
      <li><a href="/">Customer Support</a>
        <ul>
          <li><a href="/">Cloud 동향 및 소식</a></li> 
          <!--<li><a href="/m3/sub2.asp">FAQ</a></li>-->
          <li><a href="/">1:1 문의</a></li>
          <li><a href="/">문의내역조회</a></li>
          <!--<li><a href="/m3/sub5.asp">공지사항</a></li>-->
        </ul>
      </li>
      <li><a href="/">Recruit</a>
        <ul>
          <li><a href="/">인재상</a></li> 
          <li><a href="/">복리후생</a></li> 
          <li><a href="/">직무소개</a></li> 
          <li><a href="/">온라인 입사지원</a></li> 
        </ul>
      </li>
      <li><a href="/">About Us</a>
        <ul>
          <li><a href="/">회사소개</a></li> 
          <li><a href="/">History</a></li> 
          <li><a href="/">지적재산권 및 인증</a></li> 
          <li><a href="/">찾아오시는 길</a></li> 
        </ul>
      </li>
    </ul>
    <button class="btn_gnbToggle" @click="doGnbToggle">토글버튼</button>
  </div>
</template>

<script>
export default {
  name: 'Gnb',
  data: function () {
    return {
      isGnbOpened: false,
    }
  },
  mounted: function () {
    let gnbUlLiEl = document.querySelectorAll('#gnb > ul > li');
    let gnbUlLiAEl = document.querySelectorAll('#gnb > ul > li > a');
    for(let i=0; i<gnbUlLiAEl.length; i++){
      gnbUlLiAEl[i].addEventListener('mouseover', function (){
        this.parentElement.setAttribute('class','active');
        document.getElementById('header').setAttribute('class','subOpened');
        //alert('hover');
      });
      gnbUlLiAEl[i].parentElement.addEventListener('mouseleave', function (){
        this.setAttribute('class','');
        //alert('hover');
      });
    }
    document.getElementById('header').addEventListener('mouseleave', function (){
      gnbUlLiEl.forEach((function(x){ x.setAttribute('class',''); }))
      this.setAttribute('class','');
      //alert('hover');
    });
  },
  methods: {
    doGnbToggle: function(){
      this.isGnbOpened = this.isGnbOpened ? false : true;
      alert(this.isGnbOpened);
    },
  }
};
</script>
<style scoped>
#gnb{display:block;margin-left:auto;padding-right:80px;}
#gnb ul,
#gnb ul li,
#gnb ul li a{display:block;}
#gnb > ul{display:flex;flex-direction:row;}
#gnb > ul > li{display:block;position:relative;margin:0 10px;}
#gnb > ul > li > a{display:block;padding:0 10px;font-size:19px;font-weight:600;line-height:85px;}
#gnb > ul > li > ul{display:block;position:absolute;top:75px;left:50%;margin-left:-400px;width:800px;text-align:center;opacity:0;z-index:-1;transition-duration:0.3s;}
#gnb > ul > li:after{display:block;content:'';position:absolute;bottom:-2px;left:50%;width:0;height:4px;background:#44B8F2;transform:translateX(-50%);transition-duration:0.3s;}
#gnb > ul > li.active:after{width:100%;}
#gnb > ul > li.active > ul{display:block;top:85px;opacity:1;z-index:1;}
#gnb > ul > li > ul > li{display:inline-block;margin:20px;line-height:40px;}
#gnb > ul > li:nth-child(5) > ul{margin-left:-500px;}
#gnb .btn_gnbToggle{position:absolute;top:0;bottom:0;right:0;width:50px;text-indent:-9999em;background:url(/images/main/full_menu.png) no-repeat center center;border:0px none;z-index:1;}
</style>