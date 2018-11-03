<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <!-- <router-view/> -->
    <div class="sidebar">
      <div class="header">Channels</div>
      <div class="content">
        <div v-for="channel in channels" :key="channel">
          Channel {{ channel }}
        </div>
      </div>
    </div>
    <div class="main">
      <div class="header">
        <div class="title">Title</div>
        <div class="description">description</div>
      </div>
      <div class="content">
        <div class="message-container">
          <div v-for="color in colors" :key="color" :style="{ backgroundColor: '#'+color }">
            #{{ color }}
          </div>
        </div>
        <div class="input-container">
          <input type="text" name="" id="">
          <button class="btn btn-sm btn-primary">Button</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'mesh',
  data() {
    return {
      channels: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
      colors: [
        // 'Black',
        '1a1c1e',
        '4f545c',
        '36393e',
        '9099a4',
        '18191c',
        '202225',
        '222941',
        '23262a',
        '36393f',
        '2a2d32',
        '2e3033',
        '161a29',
        '040405',
        '050809',
        // 'Grey',
        '72767d',
        'b9bbbe',
        '737f8d',
        'b3b3b3',
        '747f8d',
        'cdcdcd',
        '8a8e94',
        'afafaf',
        'dadddf',
        '4f5660',
        '4d4d4d',
        '424245',
        // 'Light',
        'f6f6f7',
        'f3f3f3',
        'f7f7f7',
        'f2f2f2',
        'fcfcfc',
        'dcddde',
        // 'red',
        'd0021b',
        'cb2120',
        '8a1616',
        '24365d',
        '1b2138',
      ],
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

#app {
  height: 100vh;
  display: flex;
  flex-direction: row;
  padding: 0;
  margin: 0;
}
.sidebar {
  flex-shrink: 0;
  width: 300px;
  display: flex;
  flex-direction: column;
}
.main {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.header {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  height: 40px;
  border-bottom: 1px solid #1b1818;
  padding: 0 10px;
}
.content {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  padding: 0 10px;
}
.sidebar .header {
  background-color: #0c0c0c;
  /* background-color: #101010; */
}
.sidebar .content {
  background-color: #101010;
}
.main .header {
  background-color: #0c0c0c;
  background-color: #121213;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  /* background-color: #191919; */
}
.main .header .title {
  font-size: 14px;
  line-height: 14px;
}
.main .header .description {
  font-size: 12px;
  line-height: 12px;
  /* margin-left: 10px; */
}
.main .content {
  background-color: #181819;
  display: flex;
  flex-direction: column;
  padding: 0;
}
.main .content .message-container {
  display: flex;
  // flex-direction: column;
  flex-grow: 1;
  padding: 0 10px;
  flex-wrap: wrap;
  flex-flow: wrap;
}
.main .content .input-container {
  flex-shrink: 0;
  display: flex;
  flex-direction: row;
  padding: 10px;
  background-color: #1d1d1d;
}
.main .content .input-container input[type="text"] {
  flex-grow: 1;
  line-height: 15px;
  background-color: #181819;
  border-color: #121213;
  border-style: solid;
}
.main .content .input-container button {
  flex-shrink: 0;
}
.message-container > div {
  width: 100px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
