<template>
  <div class="boardSearch">
    <form id="searchForm" @submit.prevent="doSearch">
      <label for="keyword" class="required">키워드 검색</label>
      <!-- required="true" -->
      <input type="text" id="keyword" placeholder="검색어를 입력해주세요." v-model="keyword" />
      <button type="submit">검색</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'BoardSearch',
  data: function() {
    return {
      keyword: '',
    }
  },
  methods : {
    doSearch(e) {
      this.$emit('doKeyword', this.keyword);
    }
  }
};
</script>

<style scoped>
.boardSearch{margin-bottom:20px;text-align:right;}
.boardSearch input,
.boardSearch button{height:30px;}
</style>

