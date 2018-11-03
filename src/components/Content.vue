<template>
  <div class="main">
    <div class="header">
      <div class="title-container">
        <span class="channel-type">{{ channelType }}</span>
        <span class="title">{{ title }}</span>
        <span class="description" v-if="description">{{ description }}</span>
      </div>
      <div class="action-container">
        <input type="text" class="form-input search-input input-text" placeholder="Search">
      </div>
    </div>
    <div class="content">
      <div class="message-container">
        <div v-for="color in colors" :key="color" :style="{ backgroundColor: '#'+color }">
          #{{ color }}
        </div>
      </div>
      <div class="input-container">
        <div class="input-content">
          <button class="btn btn-sm btn-primary">+</button>
          <input type="text" class="input-text" placeholder="Message">
          <button class="btn btn-sm btn-primary">:)</button>
        </div>
      </div>
      <div class="typing-container">
        someone is typing
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content',
  props: {
    colors: Array,
  },
  data() {
    return {
      channelType: '#',
      title: 'title',
      description: 'Some description',
    };
  },
};
</script>

<style lang="scss" scoped>
.main {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
// Common
.input-text {
  line-height: 15px;
  background-color: #181819;
  // border-color: #47477a;
  border-style: solid;
  border-color: transparent;
  height: 25px;
  caret-color:#4f545c;
}
// Header
.header {
  background-color: #1d1d1d;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}
// Header - title
.header .title-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  line-height: 16px;
  flex-grow: 1;
  overflow: hidden;
}
.header .channel-type {
  margin-right: 5px;
}
.header .title {
  color: #ffffff;
  font-weight: bold;
  font-size: 16px;
}
.header .description {
  font-weight: bold;
  font-size: 12px;
  margin-left: 10px;
  padding-left: 10px;
  border-left: 1px solid gray;
  white-space: nowrap;
}
// Header - actions
.header .action-container {
  flex-shrink: 0;
  flex-wrap: nowrap;
  display: flex;
}
.header .action-container .search-input {
  width: 150px;
  transition: 0.2s linear all;
  height: 25px;
}
.header .action-container .search-input:active,
.header .action-container .search-input:focus
{
  width: 250px;
}
// Content
.content {
  background-color: #1d1d1d;
  display: flex;
  flex-direction: column;
  padding: 0;
}
.content .message-container {
  display: flex;
  // flex-direction: column;
  flex-grow: 1;
  padding: 10px 10px;
  flex-wrap: wrap;
  flex-flow: wrap;
}
.content .input-container {
  flex-shrink: 0;
  box-shadow: 0 -1px 0 0 #2a2d32;
  margin: 0 10px;
}
.content .input-content {
  display: flex;
  flex-direction: row;
  margin: 10px 0;
  padding: 5px;
  // padding-top: 10px;
  background-color: #1d1d1d;
  background-color: #181819;
  // height: 35px;
}
.content .input-container .input-text {
  flex-grow: 1;
  height: auto;
}
.content .input-container .btn {
  flex-shrink: 0;
  font-size: 20px;
}
.content .input-container .btn:hover {
  background-color: #2a2d32;
}
.content .input-container .input-text,
.content .input-container .input-text:active,
.content .input-container .input-text:focus,
.content .input-container .btn,
.content .input-container .btn:active,
.content .input-container .btn:focus {
  background-color: #1d1d1d;
  background-color: transparent;
  border-color: transparent;
  outline: none;
  box-shadow: none;
}
.content .input-container .input-text {
  margin-left: 4px;
  padding-left: 10px;
  border-left: 1px solid #808080!important;
}
// Typing container
.typing-container {
  flex-shrink: 0;
  padding: 5px 10px;
  text-align: left;
}
</style>
