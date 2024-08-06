<template>
  <div class="relative inline-block text-left">
    <div>
      <button @click="toggleDropdown" type="button" class=" inline-flex justify-center text-white w-full rounded-xl border border-gray-300 shadow-sm px-4 py-3 bg-slate-900 text-sm font-bold  hover:bg-slate-900 outline-none focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" id="menu-button" aria-expanded="true" aria-haspopup="true">
        <img :src="selectedLanguage.flag" alt="" class="w-5 h-5 mr-2">
        {{ selectedLanguage.name }}
        <i :class="['ri-arrow-down-s-line pl-2 iconk', { 'rotate-180': dropdownOpen }]" class="transition-transform duration-200"></i>
      </button>
    </div>

    <div v-show="dropdownOpen" class="origin-top-right absolute right-0 mt-2 text-white w-56 border border-gray-300 rounded-md shadow-lg  ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
      <div class="py-1 " role="none">
        <button v-for="language in languages" :key="language.code" @click="selectLanguage(language)" class="text-white block  px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-0">
          <img :src="language.flag" alt="" class="w-10 h-5 mr-2 inline bg-cover">
          {{ language.name }}
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const dropdownOpen = ref(false);
const languages = ref([
  { code: 'ru', name: 'RU', flag: 'https://upload.wikimedia.org/wikipedia/commons/d/d4/Flag_of_Russia.png' },
  { code: 'uz', name: 'O’Z', flag: 'https://upload.wikimedia.org/wikipedia/commons/0/0b/Flag_of_Uzbekistan.png' },
]);
const selectedLanguage = ref(languages.value[0]);

const toggleDropdown = () => {
  dropdownOpen.value = !dropdownOpen.value;
};

const selectLanguage = (language) => {
  selectedLanguage.value = language;
  dropdownOpen.value = false;
};
</script>

<style scoped>
.rotate-180 {
  transform: rotate(180deg);
}
</style>
