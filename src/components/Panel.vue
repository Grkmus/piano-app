<template lang='pug'>
q-card.column.q-ma-xs
  q-card-section.q-pa-sm
    .row.justify-center
      .text-h6 {{name}}
  q-separator(inset)
  q-card-section.q-pa-sm.action-container.row.no-wrap.justify-around.items-center
    slot
</template>

<script>

export default {
  props: {
    name: null,
  },
};
</script>

<style>
.action-container {
  flex-grow: 1
}
</style>
