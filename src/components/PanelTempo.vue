<template lang='pug'>
Panel(name="Tempo")
  template(v-slot)
    label.col-3(for='tempo') bpm
    q-slider.col-8(v-model="tempo" :min="0" :max="300" label)
</template>

<script>
import { inject, ref } from 'vue';
import Panel from './Panel.vue';

export default {
  name: 'PanelTempo',
  components: {
    Panel,
  },
  setup() {
    const app = inject('theApp');
    return { app, tempo: ref(120) };
  },
  watch: {
    tempo(newVal) {
      this.app.value.tempoChange(newVal);
    },
  },
};
</script>

<style>
</style>
