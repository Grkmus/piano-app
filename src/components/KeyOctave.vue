<template lang="pug">
.octave(:style='{width: `${octaveWidth}px`}')
  .white-keys
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='C' key='C' note='C')
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='D' key='D' note='D')
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='E' key='E' note='E')
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='F' key='F' note='F')
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='G' key='G' note='G')
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='A' key='A' note='A')
    key.white-key(:style='{ width: `${whiteKeyWidth}px`}' ref='B' key='B' note='B')
  .black-keys
    key.black-key(:style='{ width: `${keyWidth}px`, left:`${2 + keyWidth}px`}' ref='C#' key='C#' note='C#')
    key.black-key(:style='{ width: `${keyWidth}px`, left:`${4 + keyWidth * 3}px`}' ref='D#' key='D#' note='D#')
    key.black-key(:style='{ width: `${keyWidth}px`, left:`${6 + keyWidth* 6}px`}' ref='F#' key='F#' note='F#')
    key.black-key(:style='{ width: `${keyWidth}px`, left:`${4 + keyWidth * 8}px`}' ref='G#' key='G#' note='G#')
    key.black-key(:style='{ width: `${keyWidth}px`, left:`${keyWidth * 10}px`}' ref='A#' key='A#' note='A#')
</template>

<script>
import Key from './Key.vue';

export default {
  components: { Key },
  name: 'Octave',
  props: {
    keyWidth: Number,
    octaveWidth: Number,
  },
  computed: {
    whiteKeyWidth() { return this.keyWidth * 2; },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.octave {
  height: 100%;
  margin: 0;
  padding: 0;
  position: relative;
}
.white-keys {
  display: flex;
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  position: absolute;
}
.black-keys {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  top:0;
  left: 0;
  position: absolute;
}

.white-key {
  height: 100%;
  border: 1px solid;
  border-radius: 5px;
  background-color: whitesmoke;
  margin: 0;
  padding: 0;
  box-shadow: inset 0 0 5px #4d4c4c;
}

.black-key {
  height: calc(100% / 1.5);
  border-radius: 5px;
  background-color: rgb(49, 49, 49);
  margin: 0;
  padding: 0;
  position: absolute;
  border: 1px solid black;
  box-shadow: 0px 0px 5px #4d4c4c;
}
</style>
