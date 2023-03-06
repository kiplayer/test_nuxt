<template>
  <div class="tabPage">
      TabPage2 Component<br />
  </div>
</template>

<script>
export default {
  name: 'TabPage2',
  props: {
    title: String,
  },
};
</script>
<style>
.tabPage{padding:20px;min-height:200px;border:1px #ccc solid;}
</style>