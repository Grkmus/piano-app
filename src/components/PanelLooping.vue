<template lang='pug'>
Panel(name="Looping")
  template(v-slot)
    q-checkbox(v-model='isLooping' dense)
    q-range(
      :disable='!isLooping'
      v-model='standard'
      :min="0"
      :max="50"
      :dense='true'
      label
    )
</template>

<script>
import Panel from './Panel.vue';

export default {
  name: 'PanelLooping',
  components: {
    Panel,
  },
  data() {
    return {
      isLooping: true,
      standard: {
        min: 10,
        max: 35,
      },
    };
  },
};
</script>

<style>
</style>
