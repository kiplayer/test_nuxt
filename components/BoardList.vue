<template>
  <ul class="boardList">
    <li v-for="(item, no) in list" :key="no">
      <BoardItem v-bind="item" />
    </li>
  </ul>
</template>

<script>
import BoardItem from "~/components/BoardItem.vue";
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

<style>
.boardList{display:block;list-style:none;border:1px #ccc solid;border-bottom:0px none;}
.boardList > li{display:block;list-style:none;margin:0;padding:0;border-bottom:1px #ccc solid;}
.boardList a{display:block;text-decoration:none;}
</style>

