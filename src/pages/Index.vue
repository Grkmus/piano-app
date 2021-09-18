<template lang="pug">
.q-pa-sm.fit
  ThePanel#panel
  q-card#rest.q-pa-sm.q-ma-xs
    TheSheet(@app-ready="assingApp")
    TheKeyboard
</template>

<script>

import TheSheet from 'src/components/TheSheet.vue';
import TheKeyboard from 'src/components/TheKeyboard.vue';
import ThePanel from 'src/components/ThePanel.vue';
import { defineComponent, ref, provide } from 'vue';

export default defineComponent({
  name: 'PageIndex',
  components: {
    ThePanel,
    TheSheet,
    TheKeyboard,
  },
  setup() {
    const theApp = ref({});
    provide('theApp', theApp);
    return { theApp };
  },
  methods: {
    assingApp(theApp) {
      console.log(this);
      console.log('The app is ready', theApp);
      this.theApp.value = theApp;
      // this.$emit('app-ready-index', theApp);
      // this.index += 1;
    },
  },
});
</script>

<style>

html, body, #q-app { height: 100%; width: 100%; margin: 0; padding: 0;}
#panel {
  height: 10%;
}
#rest {
  height: 90%;
}
</style>
