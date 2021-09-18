<template lang='pug'>
#panel.row.justify-evenly
  panel-player.col
  panel-mods.col-4
  panel-tempo.col
  panel-looping.col
</template>

<script>
/*eslint-disable*/
import PanelPlayer from 'components/PanelPlayer.vue';
import PanelMods from 'components/PanelMods.vue';
import PanelTempo from 'components/PanelTempo.vue';
import PanelLooping from 'components/PanelLooping.vue';
import AboutAuthor from 'components/AboutAuthor.vue';
import { toRefs, watch, inject } from 'vue';

export default {
  name: 'Panel',
  components: {
    PanelPlayer,
    PanelMods,
    PanelTempo,
    PanelLooping,
    AboutAuthor,
  },
  setup(props) {
    const app = inject('theApp')
    console.log(app);
    return app;
  },

};
</script>

<style>
#panel {
  height: 15%;
}
</style>
