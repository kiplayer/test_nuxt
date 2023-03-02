<template>
  <section class="container boardWrap">
    <h2>게시물 쓰기</h2>
    <form id="writeForm" @submit.prevent="doSubmit">
      <ul class="formUI">
        <li>
          <label for="inputId" class="required">아이디</label>
          <input type="text" id="inputId" v-model="form.inputId" placeholder="아이디를 입력해주세요." value="" />
        </li>
        <li>
          <label for="inputName" class="required">작성자명</label>
          <input type="text" id="inputName" v-model="form.inputName" placeholder="작성자명을 입력해주세요." value="" />
        </li>
        <li>
          <label for="inputPw" class="required">비밀번호</label>
          <input type="password" id="inputPw" v-model="form.inputPw" placeholder="비밀번호를 입력해주세요." value="" />
        </li>
        <li>
          <label for="inputPwRe" class="required">비밀번호 확인</label>
          <input type="password" id="inputPwRe" v-model="form.inputPwRe" placeholder="비밀번호를 다시 입력해주세요." value="" />
        </li>
        <li>
          <label for="inputTitle" class="required">제목</label>
          <input type="text" id="inputTitle" v-model="form.inputTitle" placeholder="제목를 입력해주세요." value="" />
        </li>
        <li>
          <label for="">텍스트박스</label>
          <textarea id="inputContent" v-model="form.inputContent" placeholder="내용를 입력해주세요."></textarea>
        </li>
      </ul>
      <button type="submit">등록하기</button>
    </form>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      form: {
        inputId: '',
        inputPw: '',
        inputPwRe: '',
        inputName: '',
        inputTitle: '',
        inputContent: '',
      }
    }
  },
  methods: {
    doSubmit: function() {
      const formData = new FormData();
      for (let [key, value] of Object.entries(this.form)) {
        formData.append(key, value);
      }

      //Value Check
      if(this.form.inputId == ''){
        alert('아이디를 입력해주세요.');
        document.getElementById('inputId').focus();
        return ;
      }
      let idRole = /^[A-Za-z0-9_-]{6,20}$/;
      if(!idRole.test(this.form.inputId)) {
        alert('아이디는 영문, 숫자, 특수문자(_,-)만 사용 가능하며 6자 이상이어야 합니다.');
        document.getElementById('inputId').focus();
        return ;
      }

      let passwordRole = /^(?=.*\d)(?=.*[a-zA-Z])[0-9a-zA-Z]{8,20}/;
      if(!passwordRole.test(this.form.inputPw)) {
          alert('비밀번호는 영문, 숫자 조합만 사용 가능하며 8자 이상이어야 합니다.');
        document.getElementById('inputPw').focus();
        return ;
          return ;
      }
      if(this.form.inputPw == '' && this.form.inputPwRe == ''){
        alert('비밀번호를 입력해주세요.');
        document.getElementById('inputPw').focus();
        return ;
      }
      if(this.form.inputPw != this.form.inputPwRe){
        alert('비밀번호가 맞지 않습니다. 다시 입력해주세요.');
        document.getElementById('inputPwRe').focus();
        return ;
      }
      if(this.form.inputName == ''){
        alert('휴대폰번호를 입력해주세요.');
        return ;
      }

      alert(JSON.stringify(this.form));
      return false;
    }
  }
};
</script>

<style>
.container{margin:0 auto;width:800px;flex-direction: column;}
ul.formUI{display:block;}
ul.formUI li{display:block;margin:10px 0;list-style:none;}
ul.formUI li label{display:block;}
ul.formUI li .required:after{display:inline;content:'*';color:#ff3300;}
ul.formUI li input + label{display:inline-block;margin-right:10px;}
ul.formUI li input[type='text'],
ul.formUI li input[type='password']{padding:0 5px;width:200px;height:30px;}
</style>
