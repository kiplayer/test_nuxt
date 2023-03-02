<template>
  <ul class="boardList">
    <li v-for="(item, no) in list" :key="no">
      <BoardItem v-bind="item" />
    </li>
  </ul>
</template>

<script lang="ts">
import BoardItem from "./BoardItem.vue";
export default {
  components: {
    BoardItem,
  },
  name: 'BoardList',
  props: {
    list: Array,
    page: Number,
    count: Number,
  },
};
</script>

<style scoped>
.boardList{display:block;list-style:none;border-top:1px #ccc solid;}
.boardList > li{display:block;list-style:none;margin:0;padding:0;border-bottom:1px #ccc solid;}
.boardList a{display:block;text-decoration:none;}
</style>

