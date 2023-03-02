<template>
  <section class="container boardWrap">
    <h2>게시물 상세</h2>
    <div>
      <div v-if="isLoading">
        Loading ...
      </div>
      <div class="boardDetail">
        <div class="title">
          <b>{{ detailData.title }}</b>
          <span class="date">{{ detailData.date }}</span>
        </div>
        <div class="content">{{ detailData.content }}</div>
      </div>
      <div class="boardBtn">
        <nuxt-link class="btn" :to="{path:'/board/list'}">목록보기</nuxt-link>
        <nuxt-link class="btn" :to="{path:'/board/write', query:{id:1}}">수정하기</nuxt-link>
        <a class="btn" @click="doDelete">삭제하기</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      isLoading: true,
      detailParams: {
        no:0,
      },
      detailData: {
        no:0, 
        title:'', 
        content:'', 
        date:''
      },
    }
  },
  created() {
    // 구조 미작성
  },
  mounted() {
    // 최초 실행
    this.getDetail();
  },
  methods: {
    getDetail: async function() {
      this.isLoading = true;
      console.log(this.isLoading);

      // API 호출 영역
      console.log('----- API 호출 시작 -----');
      console.log('Params :');
      console.log(this.detailParams);

      console.log('----- API 호출 끝 -----');
      this.isLoading = false;
      console.log(this.isLoading);
      console.log('Response :');
      this.detailData = {
        no:1, 
        title:'제목'+this.$route.params.id, 
        content:'본문1', 
        date:'2023.03.02'
      };
      console.log(this.detailData);
    },
    doDelete: function() {
      if(confirm("삭제하시겠습니까?")){
        alert("삭제되었습니다.");
        this.$router.push('/board/list')
      }
    },
  },
};
</script>

<style scoped>
.container{margin:0 auto;width:800px;}
.boardDetail{display:block;}
.boardDetail .title{display:block;padding:10px 0;border-bottom:1px #ccc solid;}
.boardDetail .title b{display:block;font-size:17px;}
.boardDetail .title .date{display:block;font-size:12px;text-align:right;}
.boardDetail .content{display:block;padding:20px 0 40px;min-height:400px;}
.boardBtn{margin-top:10px;text-align:right;}
.btn{display:inline-block;padding:0 15px;font-size:14px;line-height:30px;background:#eee;border:0px none;border-radius:5px;text-decoration:none;}
</style>
