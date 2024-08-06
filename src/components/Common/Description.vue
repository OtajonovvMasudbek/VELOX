<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="max-w-[1200px] mx-auto">
    <div class="text-left mt-[20px]">
      <h2 :class="['text text-[79px] font-serif text-white opacity-30 font-semibold', headerClass, variantClass]">
        {{ text }}
      </h2>
      <p class="text-[20px] text-center font-bold max-w-[700px] text-white">
        {{ title }}
      </p>
    </div>
  </div>
</template>

<script setup>
import { defineProps, computed } from 'vue';
const props = defineProps({
  text: String,
  title: String,
  variant: {
    type: String,
    default: 'default'
  }
});

const headerClass = 'your-default-header-class';

const variantClass = computed(() => {
  switch (props.variant) {
    case 'variant1':
      return 'text-white font-bold text-[5px]';
    case 'variant2':
      return 'text-white text-[45px]';
    default:
      return '';
  }
});
</script>
