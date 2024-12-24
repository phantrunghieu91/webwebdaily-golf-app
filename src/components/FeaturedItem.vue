<script lang="ts" setup>
const props = defineProps<{
  itemData: {
    title: string;
    isNew: boolean;
    postedAt: string;
  };
}>();
</script>
<template>
  <article class="relative">
    <div class="relative">
      <span v-if="props.itemData.isNew" class="absolute z-[2] top-0 right-0 rounded-md py-1 px-2 uppercase font-bold text-sm bg-yellow-100/75 text-amber-600 tracking-widest">New</span>
      <div class="relative z-[1] w-full min-w-36 rounded-md bg-gradient-to-b from-teal-500 to-sky-300 aspect-[4/5]"></div>
      <span class="absolute z-[2] bottom-1 right-1 px-2 rounded-sm bg-gray-800 text-xs leading-5">{{ props.itemData.postedAt }}</span>
    </div>
    <h3 class="mt-2">{{ props.itemData.title }}</h3>
  </article>
</template>