<template>
  <nuxt-link :to="{path:'/board/'+no}">
    <div class="boardItem">
      <b class="title">{{ title }}</b>
      <span class="content">{{ content }}</span>
      <span class="date">{{ date }}</span>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: 'BoardItem',
  mounted() {
    // 최초 실행
  },
  props: {
    no: Number,
    title: String,
    content: String,
    date: String,
  },
};
</script>

<style scoped>
.boardItem{display:block;padding:10px;}
.boardItem .title{display:block;margin-bottom:10px;font-size:17px;}
.boardItem .content{display:block;margin-bottom:10px;}
.boardItem .date{display:block;font-size:12px;text-align:right;}
</style>

