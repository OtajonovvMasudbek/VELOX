<template>
    <header class="fixed top-0 left-0 right-0 z-10 bg-slate-900 bg-opacity-80 shadow-md">
      <nav class= "max-w-[1300px] mx-auto h-[80px]  flex justify-between px-7">
        <div class="flex items-center gap-1 text-[15px] text-white">
            <i class="ri-gallery-view-2  text-[30px] text-white"></i>
            <p class="font-bold">
                Kurslarimiz
            </p>
        </div>
        <div class="translate-x-36">
           <img class="bg-[#14191f] px-3  pt-8 pb-3 rounded-b-full"  src="https://uic.academy/images/logo.svg" alt="uic">
        </div>
       <div class="flex items-center gap-4"> 
         <Button  variant="variant2" :icon="true" text="+998 94 054 27 22" >
            <template #icon>
                <i class="ri-phone-fill text-sky-500"></i>
            </template>
         </Button>
         <LanguageSelector/>
         <Button  variant="variant1" text=" Ariza qoldirish"/>
       </div>
      </nav>
    </header>
</template>

<script setup>
    import Button from '../Common/Button.vue'
    import LanguageSelector from '../Common/LanguageSelector.vue'
</script>