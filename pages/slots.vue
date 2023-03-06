<template>
  <section class="container">
    <h2>Slot 사용법</h2>
    <child-slots>
      <template v-slot:header>
        <!-- 슬롯 헤더 위치 -->
      </template>
      <template v-slot:lnb>
        <!-- 슬롯 좌측메뉴 위치 -->
      </template>
      <br />
      컨테이너<br />
      Java 의 decorator 와 비슷한 성격<br />
      <br />
      <template v-slot:footer>
        <!-- 슬롯 푸터 위치 -->
      </template>
    </child-slots>
  </section>
</template>

<script>
import ChildSlots from '../components/ChildSlots.vue'

export default {
  name: 'App',
  components: {
    ChildSlots
  }
}
</script>