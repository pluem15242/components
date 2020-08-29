<template>
  <div id="app">
    <HelloWorld msg="โหวตเลือกที่ชอบได้เลย" />
    <hr />
    <div class="row">
      <div class="col-6">
        <img alt="Vue logo" height="400" width="500" src="https://i.pinimg.com/236x/6b/ee/fc/6beefcb0b34bb22f2314f2ca993e3c6d.jpg" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
        <img alt="Vue logo" height="400" width="500" src="https://i.pinimg.com/564x/9e/77/07/9e77078acbc2267e77a53292cc7aaeb3.jpg" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CSButton @cc="sum" />
      </div>
      <div class="col-6">
        <CSButton @cc="sum1" />
      </div>
    </div>
  </div>
</template>

<script>
import CSButton from "./components/CsButton";
import HelloWorld from "./components/HelloWorld";
export default {
  name: "App",
  components: {
    HelloWorld,
    CSButton,
  },
  data: function () {
    return {
      total1: 0,
      total2: 0,
    };
  },
  methods: {
    sum(counterValue) {
      this.total1 = counterValue;
    },
    sum1(counterValue) {
      this.total2 = counterValue;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>