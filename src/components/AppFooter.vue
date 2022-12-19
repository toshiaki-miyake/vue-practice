<script setup>

defineProps(['backgroundColor'])  

</script>

<template>
  <footer >
    <p class="copyright" :style="{ 'background-color': backgroundColor }">copyright 2021 - <slot></slot></p>
  </footer>
</template>