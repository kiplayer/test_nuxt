<template>
  <section class="container">
    <h2>Sync</h2>
    <div>
      <Sync1 @doSync1="doSync1" />
      {{ syncValue }}
      <Sync2 :data="syncValue" />
      <!-- {{ syncValue2 }} -->
      <Sync3 :data.sync="syncValue" @doSync3="doSync3" />
      <!-- <Sync3 v-bind:doSync3.sync="syncValue" /> -->
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
      syncValue:false,
    };
  }, 
  components: {
    Sync1,
    Sync2,
    Sync3,
  },
  methods: {
    doSync1: function(value) {
      this.syncValue = value;
    },
    doSync3: function(value) {
      this.syncValue = value;
    },
  },
};
</script>

<style>
.container{margin:0 auto;width:800px;}
</style>
