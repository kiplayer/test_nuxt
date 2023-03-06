<template>
  <div class="slots">
    <slot name="header">
      <div class="header">
        <span class="profile">
          <span class="name"><b>홍길동</b> 님</span>
          <a href="#">로그아웃</a>
        </span>
      </div>
    </slot>
    <slot name="lnb">
      <div class="lnb">
        <h2>메뉴</h2>
        <ul>
          <li><a href="#">메뉴1</a>
            <ul>
              <li><a href="#">메뉴1-1</a></li>
              <li><a href="#">메뉴1-2</a></li>
              <li><a href="#">메뉴1-3</a></li>
            </ul>
          </li>
          <li><a href="#">메뉴2</a>
            <ul>
              <li><a href="#">메뉴2-1</a></li>
              <li><a href="#">메뉴2-2</a></li>
              <li><a href="#">메뉴2-3</a></li>
            </ul>
          </li>
          <li><a href="#">메뉴3</a>
            <ul>
              <li><a href="#">메뉴3-1</a></li>
              <li><a href="#">메뉴3-2</a></li>
              <li><a href="#">메뉴3-3</a></li>
            </ul>
          </li>
          <li><a href="#">메뉴4</a></li>
          <li><a href="#">메뉴5</a></li>
        </ul>
      </div>
    </slot>
    <main>
      <slot></slot>
    </main>
    <slot name="footer">
      <div class="footer">
        슬롯 푸터
      </div>
    </slot>
  </div>
</template>
<script>
export default {
    name: 'ChildSlots',
}
</script>
<style>

</style>
