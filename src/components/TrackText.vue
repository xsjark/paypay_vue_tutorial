<template>
  <h1 id="track-text" v-if="isVisible">hello track</h1>
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
h1 {
    color: black
}
</style>