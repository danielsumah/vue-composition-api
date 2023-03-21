<script setup lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
import { computed, Ref, ref } from "vue";
const myNumber: Ref<number> = ref(5);
const inputText: Ref<string> = ref("");
const inputTextLength: Ref<number> = ref(0);

const numberOfCharEntered = computed(() => {
  return inputText.value.length;
});
</script>

<template>
  <div>
    <p>{{ myNumber }} is my number</p>
    <br />

    <p>{{ inputText }}</p>
    <input v-model="inputText" />
    <span> {{ numberOfCharEntered }} / 10 characters entered</span>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
