<template>
  <div class="sidebar">
    <div class="header">
      <span class="title">Server</span>
    </div>
    <div class="content">
      <div
        v-for="(channel, idx) in channels" :key="channel"
        class="channel-item" :class="{ 'active': idx === 2 }">
        <span class="channel-type">{{ idx % 2 ? '#' : '!' }}</span>
        <span class="channel-title">Channel {{ channel }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  props: {
    channels: Array,
  },
};
</script>

<style scoped lang="scss">
.sidebar {
  flex-shrink: 0;
  width: 300px;
  display: flex;
  flex-direction: column;
}
.header {
  background-color: #101010;
}
.header:hover {
  background-color: #0c0c0c;
}
.header .title {
  color: #fff;
  font-weight: bold;
  font-size: 16px;
}
.content {
  background-color: #101010;
  align-items: flex-start;
}
.channel-item {
  display: flex;
  flex-direction: row;
  width: 100%;
  margin-top: 3px;
  padding: 2px 0;
  cursor: pointer;
}
.channel-item.active,
.channel-item:hover {
  background-color: #1d1d1d;
}
.channel-type {
  margin: 0 10px;
  flex-shrink: 0;
}
.channel-title {
  flex-grow: 1;
  text-align: left;
}
</style>
