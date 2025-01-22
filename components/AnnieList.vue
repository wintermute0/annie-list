<template>
  <!-- in order to get height animation between 0 and auto. Only supported by Chrome: https://developer.chrome.com/blog/new-in-chrome-129#animate -->
  <div style="interpolate-size: allow-keywords">
    <TransitionGroup name="annie-list" tag="div">
      <slot></slot>
    </TransitionGroup>
  </div>
</template>

<script lang="ts" setup>
</script>

<style>
.annie-list-leave-active {
  transition: all 0.5s ease;
  position: relative;
  opacity: 100;
}
.annie-list-leave-from {
  left: 0px;
  opacity: 100;
}
.annie-list-leave-to {
  left: 100px;
  opacity: 0;
  height: 0px;
}
</style>
