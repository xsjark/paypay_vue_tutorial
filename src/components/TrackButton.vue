<template>
  <button id="track-button" @click="emitClick">Click Me</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'TrackButton',
  emits: ['button-click'],
  methods: {
    emitClick() {
      this.$emit('button-click');
    }
  }
});
</script>

<style scoped>
button {
  display: inline-block;
  font-size: 1.8vw;
  margin: 2em;
  padding: 8px 20px;
  line-height: 1.42857143;
  text-align: center;
  white-space: nowrap;
  cursor: pointer;
  border: 1px solid transparent;
  border-radius: 4px;
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
</style>
