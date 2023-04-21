<script setup>
import { useCounterStore } from "./stores/counter.js";
const store = useCounterStore();
</script>

<template>
  <div>
    <h1>experiment for dev vs regular dependency</h1>
    {{ store.count }}
    <button @click="store.increment()">click to increment</button>
  </div>
</template>
<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
