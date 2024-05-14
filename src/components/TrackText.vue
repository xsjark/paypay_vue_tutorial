<template>
  <div id="track-text" v-if="isVisible">
    <p>hello track</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';

export default defineComponent({
  name: 'TrackText',
  props: {
    isVisible: {
      type: Boolean as PropType<boolean>,
      required: true
    }
  }
});
</script>

<style scoped>
p {
    color: black;
    font-size: 2.8vw;
}
</style>