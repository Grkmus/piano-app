<template lang='pug'>
Panel(name="Player")
  template(v-slot)
    q-icon(name="fas fa-step-backward" size="xs")
    q-icon(v-on:click="play" name="fas fa-play" size="xs")
    q-icon(v-on:click="pause" name="fas fa-pause" size="xs")
    q-icon(v-on:click="stop" name="fas fa-stop" size="xs")
    q-icon(name="fas fa-step-forward" size="xs")
</template>

<script>
import { inject } from 'vue';
import Panel from './Panel.vue';

export default {
  name: 'PanelPlayer',
  components: {
    Panel,
  },
  setup() {
    const app = inject('theApp');
    console.log(app);
    return { app };
  },
  methods: {
    play() { this.app.value.start(); },
    stop() { this.app.value.stop(); },
    pause() { this.app.value.pause(); },
  },
};
</script>

<style>
</style>
