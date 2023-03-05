<template>
  <section class="container">
    <h2>Form</h2>
    <form id="joinForm" @submit.prevent="doSubmit">
      <ul class="formUI">
        <li>
          <label for="inputId" class="required">아이디</label>
          <!-- required="true" -->
          <input type="text" id="inputId" v-model="form.inputId" placeholder="아이디를 입력해주세요." />
          Key Event : enter, tab, delete, esc, space, up, down, left, right 
        </li>
        <li>
          <label for="inputPw" class="required">비밀번호</label>
          <input type="password" id="inputPw" v-model="form.inputPw" placeholder="비밀번호를 입력해주세요." />
        </li>
        <li>
          <label for="inputPwRe" class="required">비밀번호 확인</label>
          <input type="password" id="inputPwRe" v-model="form.inputPwRe" placeholder="비밀번호를 다시 입력해주세요." />
        </li>
        <li>
          <label for="inputTel" class="required">휴대폰번호</label>
          <input type="text" id="inputTel" v-model="form.inputTel" placeholder="휴대폰번호를 입력해주세요.(- 없이)" />
        </li>
        <li>
          <label for="">선택박스</label>
          <select id="selectBox" v-model="form.selectBox">
            <option value="1">선택1</option>
            <option value="2">선택2</option>
            <option value="3">선택3</option>
            <option value="4">선택4</option>
            <option value="5">선택5</option>
          </select>
        </li>
        <li>
          <label for="">라디오버튼</label>
          <input type="radio" id="radio1" v-model="form.inputRadio" value="1" /> <label for="radio1">라디오1</label>
          <input type="radio" id="radio2" v-model="form.inputRadio" value="2" /> <label for="radio2">라디오2</label>
          <input type="radio" id="radio3" v-model="form.inputRadio" value="3" /> <label for="radio3">라디오3</label>
        </li>
        <li>
          <label for="">체크박스</label>
          <input type="checkbox" id="check1" v-model="form.inputCheck1" value="1" /> <label for="check1">체크박스1</label>
          <input type="checkbox" id="check2" v-model="form.inputCheck2" value="2" /> <label for="check2">체크박스2</label>
          <input type="checkbox" id="check3" v-model="form.inputCheck3" value="3" /> <label for="check3">체크박스3</label>
        </li>
        <li>
          <label for="">텍스트박스</label>
        </li>
      </ul>
      <input type="submit" value="등록하기">
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
        inputTel: '010',
        selectBox: '1',
        inputRadio: '2',
        inputCheck1: '',
        inputCheck2: '',
        inputCheck3: '3',
      }
    }
  },
  methods: {
    doSubmit: function() {
      const formData = new FormData();
      for (let [key, value] of Object.entries(this.form)) {
        formData.append(key, value?value.toString():'');
      }

      //Value Check
      if(this.form.inputId == ''){
        alert('아이디를 입력해주세요.');
        document?.getElementById('inputId')?.focus();
        return ;
      }
      let idRole = /^[A-Za-z0-9_-]{6,20}$/;
      if(!idRole.test(this.form.inputId)) {
        alert('아이디는 영문, 숫자, 특수문자(_,-)만 사용 가능하며 6자 이상이어야 합니다.');
        document?.getElementById('inputId')?.focus();
        return ;
      }

      let passwordRole = /^(?=.*\d)(?=.*[a-zA-Z])[0-9a-zA-Z]{8,20}/;
      if(!passwordRole.test(this.form.inputPw)) {
          alert('비밀번호는 영문, 숫자 조합만 사용 가능하며 8자 이상이어야 합니다.');
        document?.getElementById('inputPw')?.focus();
        return ;
          return ;
      }
      if(this.form.inputPw == '' && this.form.inputPwRe == ''){
        alert('비밀번호를 입력해주세요.');
        document?.getElementById('inputPw')?.focus();
        return ;
      }
      if(this.form.inputPw != this.form.inputPwRe){
        alert('비밀번호가 맞지 않습니다. 다시 입력해주세요.');
        document?.getElementById('inputPwRe')?.focus();
        return ;
      }
      if(this.form.inputTel == ''){
        alert('휴대폰번호를 입력해주세요.');
        return ;
      }

      alert(JSON.stringify(this.form));
      return false;
    }
  }
};
</script>

<style scoped>
.container{margin:0 auto;width:800px;flex-direction: column;}
ul.formUI{display:block;}
ul.formUI li{display:block;margin:10px 0;list-style:none;}
ul.formUI li label{display:block;}
ul.formUI li .required:after{display:inline;content:'*';color:#ff3300;}
ul.formUI li input + label{display:inline-block;margin-right:10px;}
ul.formUI li input[type='text'],
ul.formUI li input[type='password']{padding:0 5px;width:200px;height:30px;}
</style>
