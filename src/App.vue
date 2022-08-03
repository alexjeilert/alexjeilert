<script setup lang="ts">
import Item from './components/Item.vue'
</script>

<template>

    <div className="fixed top-0 left-0 h-screen w-16 bg-slate-500 m-0 flex flex-col text-white shadow-lg">
      ffff


    </div>
<div className="bg-white text-gray-600"> fff


</div>
    <Item />

  
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
