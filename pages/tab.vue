<template>
  <section class="container">
    <h2>탭 구현</h2>
    <div>
      <div class="tabWrap">
        <ul class="tabBar">
          <li :class="doTabClass(1)"><a href="#" v-on:click="doTabMove(1)">탭1</a></li>
          <li :class="doTabClass(2)"><a href="#" v-on:click="doTabMove(2)">탭2</a></li>
          <li :class="doTabClass(3)"><a href="#" v-on:click="doTabMove(3)">탭3</a></li>
        </ul>
        <TabPage1 v-if="tabNo == 1" />
        <TabPage2 v-if="tabNo == 2" />
        <TabPage3 v-if="tabNo == 3" />
      </div>
    </div>
  </section>
</template>

<script>
import TabPage1 from "../components/TabPage1.vue";
import TabPage2 from "../components/TabPage2.vue";
import TabPage3 from "../components/TabPage3.vue";
export default {
  data: function() {
    return {
      tabNo: 1,
    }
  },
  methods: {
    doTabClass: function(targetNo) {
      if(this.tabNo == targetNo){
        return 'active';
      }else{
        return ;
      }
    },
    doTabMove: function(targetNo) {
      this.tabNo = targetNo;
    }
  },
  components: {
    TabPage1,
    TabPage2,
    TabPage3,
  },
};
</script>

<style>
.container{margin:0 auto;width:800px;}
.tabWrap{}
.tabBar{display:flex;flex-direction:row;margin-bottom:10px;}
.tabBar li{display:block;margin-right:5px;}
.tabBar li a{display:block;padding:0 30px;line-height:40px;color:#999;background:#eee;border:1px #ccc solid;border-bottom:1px #ccc solid;}
.tabBar li.active a{color:#000;background:#fff;}
</style>
