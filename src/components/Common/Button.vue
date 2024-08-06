<template>
    <button :class="buttonClass">
      <slot name="icon" v-if="hasIcon"></slot>
      {{ text }}
    </button>
  </template>
  
  <script setup>
  import { defineProps, computed } from "vue";
  
  const props = defineProps({
    text: String,
    variant: {
      type: String,
      default: '',
    },
    icon: {
      type: Boolean,
      default: false,
    }
  });
  
  const buttonClass = computed(() => {
    let baseClass = "text-white relative font-semibold text-lg px-[16px] py-[7px] rounded-2xl flex items-center";
    if (props.variant === 'variant1') {
      return `${baseClass} bg-[#1d71ee] hover:shadow-sm hover:shadow-white`;
    } else if (props.variant === 'variant2') {
      return `${baseClass} border border-spacing-2 hover:shadow-sm hover:shadow-white`;
    } else {
      return baseClass;
    }
  });
  
  const hasIcon = computed(() => props.icon);
  </script>
  