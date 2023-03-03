<template>
  <section class="container">
    <h2>계산기</h2>
    <div class="calculatorWrap">
      <div class="expression">
        {{ display }}
      </div>
      <div class="temp">
        {{ resultTemp }}
      </div>
      <div class="pad">
        <a href="#" @click="doClick" class="btn_control">AC</a>
        <a href="#" @click="doClick" class="btn_control">C</a>
        <a href="#" @click="doClick" class="btn_control">CE</a>
        <a href="#" @click="doClick" class="btn_operator">/</a>
        <a href="#" @click="doClick" class="btn_number">1</a>
        <a href="#" @click="doClick" class="btn_number">2</a>
        <a href="#" @click="doClick" class="btn_number">3</a>
        <a href="#" @click="doClick" class="btn_operator">*</a>
        <a href="#" @click="doClick" class="btn_number">4</a>
        <a href="#" @click="doClick" class="btn_number">5</a>
        <a href="#" @click="doClick" class="btn_number">6</a>
        <a href="#" @click="doClick" class="btn_operator">-</a>
        <a href="#" @click="doClick" class="btn_number">7</a>
        <a href="#" @click="doClick" class="btn_number">8</a>
        <a href="#" @click="doClick" class="btn_number">9</a>
        <a href="#" @click="doClick" class="btn_operator">+</a>
        <span></span>
        <a href="#" @click="doClick" class="btn_number">0</a>
        <span></span>
        <a href="#" @click="doClick" class="btn_operator">=</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      display:'',
      result:0,
      resultTemp:'',
    }
  },
  mounted() {

  },
  methods: {
    doClick: function(e) {

      console.log(e);
      console.log(e.target.innerText);
      console.log(e.target.getAttribute('class'));

      const clickEl = e.target;
      let type;
      let value = clickEl.innerText;
      switch(clickEl.getAttribute('class')){
        case 'btn_number': 
          type = 'number'; 
          this.display += value; 
          break;
        case 'btn_control': 
          type = 'control'; 
          if(this.display.length == 0){
            alert('삭제할 식이 없습니다.');
            return ;
          }
          switch(value){
            case 'AC': 
              this.display = undefined;
              this.result = undefined;
              break;
            case 'C': 
              this.display = '';
              break;
            case 'CE': 
              this.display = this.display.slice(0, -1).trim();
              break;
            case '<': 
              this.display = this.display.slice(0, -1).trim();
              break;
          }
          break;
        case 'btn_operator': 
          type = 'operator'; 
          this.display += ' '+value+' '; 
          break;
      }

      if(type == 'number'){
        this.result = eval(this.display);
        this.resultTemp = this.result.toString().replace(/\B(?<!\.\d*)(?=(\d{3})+(?!\d))/g, ",");
      }
      if(value == '='){
        //this.display = eval(this.display).toString();
        this.display = this.resultTemp;
      }

    },
  }
};
</script>

<style>
.container{margin:0 auto;width:800px;}
.calculatorWrap{width:255px;}
.calculatorWrap .expression{margin-bottom:10px;padding:15px;height:20px;background:#eee;border:1px #ccc solid;border-radius:5px;}
.calculatorWrap .temp{margin:10px 0;font-size:12px;color:#aaa;}
.calculatorWrap .pad{
    display: grid;
    width:255px;
    grid-template-columns: repeat(4, 60px);
    grid-auto-rows: 60px;
    grid-gap: 5px;
}
.calculatorWrap .pad a{display:block;font-size:21px;font-weight:bold;text-align:center;line-height:65px;background:#eee;border-radius:5px;}
.calculatorWrap .pad a.btn_operator{background-color:#ffcbcb;}
.calculatorWrap .pad a.btn_control{background-color:#9efdff;}
</style>
