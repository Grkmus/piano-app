<template lang='pug'>
q-card.q-ma-xs.q-pt-xs
  .row.justify-center
    .text-h7 {{name}}
  q-separator(inset)
  q-card-actions.no-wrap.justify-around(align="center")
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
</style>
