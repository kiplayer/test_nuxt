<template>
  <section class="container boardWrap">
    <h2>게시판</h2>
    <div>
      <BoardSearch @doKeyword="doKeyword" />
      <div v-if="isLoading">
        Loading ...
      </div>
      <div v-else>
        <div v-if="listParams.keyword != ''" class="filter">
          '{{ listParams.keyword }}' 검색결과
        </div>
        <BoardList v-bind="listData" />
      </div>
      <div class="boardListBtn">
        <nuxt-link :to="{path:'/board/write'}">[글쓰기]</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
import BoardSearch from "~/components/BoardSearch.vue";
import BoardList from "~/components/BoardList.vue";
export default {
  components: {
    BoardSearch,
    BoardList,
  },
  data() {
    return {
      isLoading: true,
      listParams: {
        keyword: '',
        page: 1,
        limit: 20,
      },
      listData: {
        list: [],
        page: 1,
        count: 0,
      },
    }
  },
  created() {
    // 구조 미작성
  },
  mounted() {
    // 최초 실행
    this.getList();
  },
  methods: {
    getList: async function() {
      this.isLoading = true;
      console.log(this.isLoading);

      // API 호출 영역
      console.log('----- API 호출 시작 -----');
      console.log('Params :');
      console.log(this.listParams);

      console.log('----- API 호출 끝 -----');
      this.isLoading = false;
      console.log(this.isLoading);
      console.log('Response :');
      this.listData = {
        list:[
          {no:1, title:'제목1', content:'본문1', date:'2023.03.02'},
          {no:2, title:'제목2', content:'본문2', date:'2023.03.02'},
          {no:3, title:'제목3', content:'본문3', date:'2023.03.02'},
          {no:4, title:'제목4', content:'본문4', date:'2023.03.02'},
          {no:5, title:'제목5', content:'본문5', date:'2023.03.02'},
        ],
        page:1,
        count:5,
      };
      console.log(this.listData);
    },
    doKeyword: function(value) {
      this.listParams.keyword = value;
      this.getList();
    }
  },
};
</script>

<style scoped>
.container{margin:0 auto;width:800px;}
.boardWrap h2{margin:0 0 20px;}
</style>
