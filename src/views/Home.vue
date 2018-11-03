<template>
  <div class="home">
    <Sidebar :channels="channels"/>
    <ContentItem :colors="colors" />
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue';
import ContentItem from '@/components/Content.vue';

export default {
  name: 'Home',
  data() {
    return {
      channels: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
      colors: [
        // 'Black',
        '040405',
        '050809',
        '0c0c0c',
        '101010',
        '18191c',
        '1a1c1e',
        '1d1d1d',
        '1b1818',
        '202225',
        '161a29',
        '1b2138',
        '222941',
        '24365d',
        '23262a',
        '2a2d32',
        '2e3033',
        '2f3136',
        '36393e',
        '36393f',
        '4f545c',
        '4f5660',
        // 'Grey',
        '737f8d',
        '747f8d',
        '9099a4',
        '72767d',
        'afafaf',
        'b3b3b3',
        'b9bbbe',
        'cdcdcd',
        'dadddf',
        'dcddde',
        '8a8e94',
        '424245',
        '4d4d4d',
        '#2c3e50',
        '#42b983',
        // 'Light',
        'f2f2f2',
        'f3f3f3',
        'f6f6f7',
        'f7f7f7',
        'fcfcfc',
        // 'red',
        '8a1616',
        'cb2120',
        'd0021b',
      ],
    };
  },
  components: {
    Sidebar,
    ContentItem,
  },
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  padding: 0;
  margin: 0;
  color: #a2a2a2;
}
</style>
