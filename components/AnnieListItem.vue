<template>
  <div
    :class="{
      'animate-fade-up': oneTimeAnimationClass,
      'animate-ease-in-out': oneTimeAnimationClass,
      'animate-duration-1000': oneTimeAnimationClass,
    }"
  >
    <div
      @click="onclick"
      :class="{ 'h-fit': expanded, 'h-[4rem]': !expanded, 'py-[16px]': true }"
      class="overflow-hidden transition-all duration-500 ease-in-out shadow rounded-xl m-2 p-4 bg-white"
    >
      <div>
        <div class="text-3xl font-bold" >Title</div>
        <div class="mt-4">
          Promotion an ourselves up otherwise my. High what each snug rich far yet easy. In companions inhabiting mr
          principles at insensible do.
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
let oneTimeAnimationClass = ref(true);
let expanded = ref(true);

onMounted(() => {
  setTimeout(() => {
    oneTimeAnimationClass.value = false;
  }, 1100);
});

let onclick = () => {
  expanded.value = !expanded.value;
};
</script>
