<template>
  <section class="container">
    <h2>v-on Events</h2>
    <div>
      <ul>
        <li><button v-on:click="doEvent('click')">click</button></li>
        <li><input type="text" v-on:keyup.enter="doEvent('keyup.enter')" placeholder="enter"></li>
        <li><input type="text" v-on:keyup.page-down="doEvent('keyup.page-down')" placeholder="page-down"></li>
        <li><input type="text" v-on:keyup.esc="doEvent('keyup.esc')" placeholder="esc"></li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    doEvent: function(actionText) {
      alert(actionText);
    }
  }
};
</script>

<style>
.container{margin:0 auto;width:800px;}
</style>
