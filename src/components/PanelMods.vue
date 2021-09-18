<template lang='pug'>
Panel(name="Mods")
  template(v-slot)
    label(for='play-along') Play along
    input#play-along(type='radio' name='mode' value='playAlong')
    label(for='wait-input') Wait for input
    input#wait-input(type='radio' name='mode' value='waitInput')
    q-separator(vertical)
    label(for='left-hand') Left Hand
    input#left-hand(type='checkbox' name='left-hand' value='leftHand')
    label(for='right-hand') Right Hand
    input#right-hand(type='checkbox' name='left-hand' value='rightHand')
</template>

<script>
import Panel from './Panel.vue';

export default {
  name: 'PanelMods',
  components: {
    Panel,
  },
};
</script>

<style>
label {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
