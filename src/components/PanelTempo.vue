<template lang='pug'>
Panel(name="Tempo")
  template(v-slot)
    label(for='tempo') bpm
    input#tempo(type='range' name='tempo' min='1' max='240' step='1')
</template>

<script>
import Panel from './Panel.vue';

export default {
  name: 'PanelTempo',
  components: {
    Panel,
  },
};
</script>

<style>
</style>
