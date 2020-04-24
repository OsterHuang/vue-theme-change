<template>
  <div id="app" :class="themeName">
    <button @click="changeLightColor">淺色</button>
    <button @click="changeDarkColor">深色</button>
    <img alt="Vue logo" src="./assets/logo.png">

    <div class="root">
      我是誰？
      <div class="root-title">
        化文與組織
      </div>
      <div class="root-content">
        今天有幾個人在這邊加班的嗎？
        <div class="remark">
          Javascript, Java, SCSS, SASS, stylus, 
        </div>
        別再加班啦，趕快下班洗洗睡…
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      themeName: 'theme-light'
    }
  },
  methods: {
    changeLightColor() {
      this.themeName = 'theme-light'
    },
    changeDarkColor() {
      this.themeName = 'theme-dark'
    }
  }
}
</script>

<style lang="scss">
@import "./styles/theme/light.scss";
@import "./styles/theme/dark.scss";

.root {
  padding: 16px;
  border: 1px solid var(--main-color-1);
  background-color: var(--main-color-2);
  color: var(--secondary-color-1);

  .root-title {
    font-size: 36px;
    font-weight: bold;
    color: var(--secondary-color-3);
  }

  .root-content {
    padding: 24px;
    border-top: 1px solid var(--primary-color);
    font-size: 14px;

    .remark {
      margin: 10px 0px;
      padding: 20px;
      background-color: var(--main-color-3);
    }
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
