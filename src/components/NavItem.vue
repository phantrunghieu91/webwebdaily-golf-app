<script lang="ts" setup>
import { Icon } from '@iconify/vue';
import { computed, defineEmits } from 'vue';

const props = defineProps<{
  itemData: {
    icon: string;
    text: string;
    active: boolean;
  },
  index: number;
}>();
const emit = defineEmits<{
  'handleClick': [index: number]
}>();
const handleClick = () => {
  emit('handleClick', props.index);
};
const classes = computed(() => {
  return {
    'opacity-100 after:absolute after:w-1 after:h-1 after:bg-white after:rounded-full after:-bottom-2 after:left-1/2 after:-translate-x-1/2': props.itemData.active,
    'opacity-50': !props.itemData.active,
  };
});

</script>
<template>
  <li class="relative grid place-items-center gap-1 cursor-pointer hover:opacity-100 transition-opacity duration-300" :class="classes" @click="handleClick">
    <Icon :icon="props.itemData.icon" style="font-size: 1.25rem" />
    <span>{{ props.itemData.text }}</span>
  </li>
</template>