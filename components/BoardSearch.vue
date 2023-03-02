<template>
  <div class="boardSearch">
    <form id="searchForm" @submit.prevent="doSearch">
      <label for="keyword" class="required">키워드 검색</label> 
      <!-- required="true" -->
      <input type="text" id="keyword" placeholder="검색어를 입력해주세요." v-model="keyword" class="btn" />
      <button type="submit" class="btn">검색</button>
      <a @click="doReset" class="btn">초기화</a>
    </form>
  </div>
</template>

<script lang="ts">
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
      this.keyword = '';
    },
    doReset: function() {
      this.$emit('doKeyword', '');
    },
  }
};
</script>

<style scoped>
.boardSearch{margin-bottom:20px;text-align:right;}
.boardSearch input,
.boardSearch button,
.boardSearch a{display:inline-block;height:30px;box-sizing:border-box;}
</style>

