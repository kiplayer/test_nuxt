<template>
  <section class="container">
    <div>
      <nuxt-link to="/">[메인화면]</nuxt-link>
    </div>
    <div>
      <sample-div title="title1" />
      <sample-div title="title2" />
      <sample-div title="title3" />
      <sample-div title="title4" />
      <sample-div title="title5" />
      <div>div div div div div div div div div div div div div div div div div div div div</div>
      <p>p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p</p>
      <span>span span span span span span span span span span span span span span span span</span>
      <ul>
        <li>li</li>
        <li>li</li>
        <li>li</li>
        <li>li</li>
        <li>li</li>
      </ul>
      <ol>
        <li>li</li>
        <li>li</li>
        <li>li</li>
        <li>li</li>
        <li>li</li>
      </ol>
      <dl>
        <dt>dt</dt>
        <dd>dd</dd>
        <dt>dt</dt>
        <dd>dd</dd>
        <dt>dt</dt>
        <dd>dd</dd>
      </dl>
      <form>
        <input type="text" id="" name="" placeholder="placeholder" value="" />
        <input type="number" id="" name="" placeholder="placeholder" value="" />
        <input type="tel" id="" name="" placeholder="placeholder" value="" />
        <select id="" name="">
          <option value="option">option</option>
          <option value="option">option</option>
          <option value="option">option</option>
          <option value="option">option</option>
          <option value="option">option</option>
        </select>
        <textarea id="" name="">textarea</textarea>
      </form>
    </div>
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
p{margin:10px 0;}
/* li{float:left;} */
input{width:100px;height:30px;}
select{width:100px;height:30px;}
textarea{width:100px;height:100px;}
</style>
