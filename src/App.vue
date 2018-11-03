<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
    </div> -->
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'mesh',
  data() {
    return {
    };
  },
};
</script>

<style lang="scss">
@import '@/../../node_modules/spectre.css/dist/spectre.css';
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100vh;
  display: flex;
  flex-grow: 1;
}
.header {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  height: 50px;
  padding: 0 10px;
  box-shadow: 0 1px 0 0 #050809;
}
.content {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  margin-top: 1px;
  padding: 0 10px;
}
.message-container > div {
  width: 100px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
