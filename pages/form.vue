<template>
  <section class="container">
    <form>
      <ul class="formUI">
        <li>
          <label for="" class="required">아이디</label>
          <input type="text" id="inputId" name="" placeholder="아이디를 입력해주세요." value="" required="true" />
        </li>
        <li>
          <label for="" class="required">비밀번호</label>
          <input type="password" id="inputPw" name="" placeholder="비밀번호를 입력해주세요." value="" required="true" />
        </li>
        <li>
          <label for="" class="required">비밀번호 확인</label>
          <input type="password" id="inputPwRe" name="" placeholder="비밀번호를 다시 입력해주세요." value="" required="true" />
        </li>
        <li>
          <label for="" class="required">휴대폰번호</label>
          <input type="text" id="inputTel" name="" placeholder="휴대폰번호를 입력해주세요." value="" required="true" />
        </li>
        <li>
          <label for="">선택박스</label>
        </li>
        <li>
          <label for="">라디오버튼</label>
          <input type="radio" id="radio1" name="inputRadio" value="1" checked="true" /> <label for="radio1">라디오1</label>
          <input type="radio" id="radio2" name="inputRadio" value="2" /> <label for="radio2">라디오2</label>
          <input type="radio" id="radio3" name="inputRadio" value="3" /> <label for="radio3">라디오3</label>
        </li>
        <li>
          <label for="">체크박스</label>
          <input type="checkbox" id="check1" name="inputCheck" value="1" checked="true" /> <label for="check1">체크박스1</label>
          <input type="checkbox" id="check2" name="inputCheck" value="2" /> <label for="check2">체크박스2</label>
          <input type="checkbox" id="check3" name="inputCheck" value="3" /> <label for="check3">체크박스3</label>
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
import AppLogo from "~/components/AppLogo.vue";
import sampleDiv from "~/components/sampleDiv.vue";
export default {
  components: {
    AppLogo,
    sampleDiv,
  },
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
