<template>
  <div>
    <button class="border shadow rounded-full m-2 p-2" @click="itemCount++">Add Item</button>
    <button class="border shadow rounded-full m-2 p-2" @click="itemCount--">Remove Item</button>
  </div>
  <AnnieList>
    <AnnieListItem v-for="i in itemCount" :key="i" :style="{ 'animation-delay': i * 100 + 'ms' }" />
  </AnnieList>
</template>

<script lang="ts" setup>
let itemCount = ref(3);
</script>

<style></style>
