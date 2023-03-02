<template>
  <section class="container">
    <h2>Html Tag</h2>
    <div>
      <AppLogo />
      <p>Route Query ID : {{ $route.query.id }}</p>
      <sample-div title="title1" />
      <sample-div title="title2" />
      <sample-div title="title3" />
      <sample-div title="title4" />
      <sample-div title="title5" />
      <div>div div div div div div div div div div div div div div div div div div div div</div>
      <p>p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p p</p>
      <span>span span span span span span span span span span span span span span span span</span>
      <ul>
        <li>ul - li</li>
        <li>ul - li</li>
        <li>ul - li</li>
        <li>ul - li</li>
        <li>ul - li</li>
      </ul>
      <ol>
        <li>ol - li</li>
        <li>ol - li</li>
        <li>ol - li</li>
        <li>ol - li</li>
        <li>ol - li</li>
      </ol>
      <dl>
        <dt>dl - dt</dt>
        <dd>dl - dd</dd>
        <dt>dl - dt</dt>
        <dd>dl - dd</dd>
        <dt>dl - dt</dt>
        <dd>dl - dd</dd>
      </dl>
      <form>
        <input type="text" id="" name="" placeholder="placeholder" />
        <input type="number" id="" name="" placeholder="placeholder" />
        <input type="tel" id="" name="" placeholder="placeholder" />
        <select id="" name="">
          <option value="option">option</option>
          <option value="option">option</option>
          <option value="option">option</option>
          <option value="option">option</option>
          <option value="option">option</option>
        </select>
        <textarea id="" name="">textarea</textarea>
        <img src>
      </form>
    </div>
  </section>
</template>

<script>
import AppLogo from "../../components/AppLogo.vue";
import sampleDiv from "../../components/sampleDiv.vue";
export default {
  components: {
    AppLogo,
    sampleDiv,
  },
};
</script>

<style>
.container{margin:0 auto;width:800px;}
p{margin:10px 0;}
/* li{float:left;} */
input{width:100px;height:30px;}
select{width:100px;height:30px;}
textarea{width:100px;height:100px;}
</style>
