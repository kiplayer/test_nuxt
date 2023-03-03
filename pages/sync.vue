<template>
  <section class="container">
    <h2>Sync</h2>
    <div>
      <Sync1 @doSync1="doSync1" />
      {{ syncValue1 }}
      <Sync2 :data="syncValue1" @doSync2="doSync2" />
      <!-- {{ syncValue2 }} -->
      <Sync3 />
    </div>
  </section>
</template>

<script>
import Sync1 from "../components/Sync1.vue";
import Sync2 from "../components/Sync2.vue";
import Sync3 from "../components/Sync3.vue";
export default {
  data() {
    return {
      syncValue1:false,
      syncValue2:false,
      syncValue3:false,
    };
  }, 
  components: {
    Sync1,
    Sync2,
    Sync3,
  },
  methods: {
    doSync1: function(value) {
      this.syncValue1 = value;
    },
    doSync2: function(value) {
      this.syncValue2 = value;
    },
  },
};
</script>

<style>
.container{margin:0 auto;width:800px;}
</style>
