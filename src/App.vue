<template>
  <div id="app">
    <TrackButton @button-click="showText" />
    <TrackText :isVisible="isTextVisible" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import TrackButton from './components/TrackButton.vue';
import TrackText from './components/TrackText.vue';

export default defineComponent({
  name: 'App',
  components: {
    TrackButton,
    TrackText
  },
  setup() {
    const isTextVisible = ref(false);

    const showText = () => {
      isTextVisible.value = true;
    };

    return {
      isTextVisible,
      showText
    };
  }
});
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
