<template>
  <section class="container">
    <h2>테이블</h2>
    <div>
      <h4>기본 목록</h4>
      <div class="tableWrap">
        <table class="list">
          <colgroup>
            <col class="w20p">
            <col class="w20p">
            <col>
          </colgroup>
          <thead>
            <tr>
              <th scope="col">항목1</th>
              <th scope="col">항목2</th>
              <th scope="col">항목3</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>값1</td>
              <td>값2</td>
              <td>값3</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h4>목록 상단의 단위항목 추가</h4>
      <div class="tableUnit">
        <span>단위 : 00</span>
      </div>
      <div class="tableWrap">
        <table class="list">
          <colgroup>
            <col>
            <col>
            <col>
          </colgroup>
          <thead>
            <tr>
              <th scope="col">항목1</th>
              <th scope="col">항목2</th>
              <th scope="col">항목3</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>값1</td>
              <td>값2</td>
              <td>값3</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h4>셀 문자 정렬</h4>
      <div class="tableWrap">
        <table class="list">
          <thead>
            <tr>
              <th scope="col">항목1</th>
              <th scope="col">항목2</th>
              <th scope="col">항목3</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h4>테이블 스크롤 기능</h4>
      <div class="tableWrap useScroll" style="height:300px;">
        <table class="list">
          <thead>
            <tr>
              <th scope="col">항목1</th>
              <th scope="col">항목2</th>
              <th scope="col">항목3</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
            <tr>
              <td class="left">좌측정렬</td>
              <td class="right">우측정렬</td>
              <td class="number">000,000</td>
            </tr>
          </tbody>
        </table>
      </div>

      <h4>기본 폼</h4>
      <div class="tableWrap">
        <table class="form">
          <colgroup>
            <col>
            <col>
          </colgroup>
          <tbody>
            <tr>
              <th scope="row"><label for="">라벨</label></th>
              <td>
                <input type="text" name="" id="">
                <a href="#" class="btn_inline">조회</a>
              </td>
            </tr>
            <tr>
              <th scope="row"><label for="">라벨</label></th>
              <td><input type="text" name="" id=""></td>
            </tr>
          </tbody>
        </table>
      </div>

      <h4>열 추가</h4>
      <div class="tableUnit">
        <span>단위 : 00</span>
      </div>
      <div class="tableWrap">
        <table class="form">
          <colgroup>
            <col>
            <col>
            <col>
            <col>
          </colgroup>
          <tbody>
            <tr>
              <th scope="row"><label for="">라벨</label></th>
              <td><input type="text" name="" id=""></td>
              <th scope="row"><label for="">라벨</label></th>
              <td><input type="text" name="" id=""></td>
            </tr>
            <tr>
              <th scope="row"><label for="">라벨</label></th>
              <td>
                <input type="text" name="" id="">
                <a href="#" class="btn_inline">조회</a>
              </td>
              <th scope="row"><label for="">라벨</label></th>
              <td>
              </td>
            </tr>
          </tbody>
        </table>
      </div>

      <h4>셀 안의 다수 멀티박스</h4>
      <div class="tableWrap">
        <table class="form">
          <colgroup>
            <col>
            <col>
          </colgroup>
          <tbody>
            <tr>
              <th scope="row"><label for="">라벨</label></th>
              <td>
                <input type="text" name="" id="">
                <a href="#" class="btn_inline">조회</a>
              </td>
            </tr>
          </tbody>
        </table>
      </div>

    </div>
  </section>
</template>

<script>
</script>

<style>
.container{margin:0 auto;width:800px;}

.tableTitle{position:relative;font-size:16px;height:40px;text-align:center;}
.tableTitle:after{display:block;content:'';clear:both;}
.tableTitle h4,
.tableTitle h5,
.tableTitle h6{display:block;float:left;margin:0;font-size:18px;line-height:40px;}
.tableTitle .btnArea{position:absolute;top:5px;right:0;margin:0 !important;}
.tableUnit{margin-bottom:10px;text-align:right;}
.tableOption{margin:10px 0;}
.tableOption:after{display:block;content:'';clear:both;}
.tableOption .left{float:left;text-align:left;}
.tableOption .right{float:right;text-align:right;}
.tableOption .total{display:inline-block;margin:0 20px;line-height:30px;vertical-align:top;}
.tableOption .total b{display:inline-block;margin-right:20px;}

.tableWrap{margin-bottom:20px;}
.tableWrap.useScroll{position:relative;border:1px #d2d2d2 solid;overflow-y:scroll;}
.tableWrap.useScroll table{margin-top:-1px;border-left:0px none;}
.tableWrap.noMargin{margin-bottom:0;}
.tableWrap table{width:100%;border-top:1px #d2d2d2 solid;border-left:1px #d2d2d2 solid;border-spacing:0;}
.tableWrap table th,
.tableWrap table td{padding:10px;font-weight:normal;border-bottom:1px #d2d2d2 solid;border-right:1px #d2d2d2 solid;box-sizing:border-box;}
.tableWrap table thead th{background:#ebebeb;font-weight:normal;}
.tableWrap table.list th,
.tableWrap table.list td{text-align:center;}
.tableWrap table.form th{padding:5px 15px;text-align:left;}
.tableWrap table.form td{padding:5px 5px;/*line-height:36px;*/text-align:left;}
.tableWrap table.view th,
.tableWrap table.view td{text-align:left;}
.tableWrap table th.left,
.tableWrap table td.left{text-align:left !important;}
.tableWrap table th.right,
.tableWrap table td.right{text-align:right !important;}
.tableWrap table th.center,
.tableWrap table td.center{text-align:center !important;}
.tableWrap table th.number,
.tableWrap table td.number{padding-right:20px;text-align:right !important;}
.tableWrap table.form th.required:before{display:inline-block;content:'*';margin-left:-8px;width:8px;font-size:14px;color:#e6242c;vertical-align:middle;}
.tableWrap.noBorder{margin-left:-30px;}
.tableWrap.noBorder table{border:0px none !important;}
.tableWrap.noBorder table th{padding:5px 10px 5px 30px !important;border:0px none !important;}
.tableWrap.noBorder table td{padding:5px 0 !important;/*line-height:36px;*/border:0px none !important;}
.tableWrap.center,
.tableWrap.center.noBorder{margin:0 auto;}
.tableWrap.center.noBorder table{margin-left:-30px;}

.tableWrap input[type='text'],
.tableWrap input[type='password']{padding:0 5px;width:200px;height:30px;}
.tableWrap textarea{width:100%;min-height:300px;}
.tableWrap .btn_inline{display:inline-block;padding:0 10px;font-size:14px;color:#000;height:30px;line-height:30px;background:#eee;border-radius:5px;border:0px none;vertical-align:middle;text-decoration:none;}
</style>
