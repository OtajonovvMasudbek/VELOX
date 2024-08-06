<template>
    <div class="bg-[url('https://uic.academy/banner_1.jpg')] bg-dark hero relative bg-cover min-h-screen flex justify-center items-center">
      <div class="absolute inset-0 bg-blue-950 opacity-70 flex flex-col justify-center items-center text-center">
        <Description class="text" title="13 yillik tajriba, 200dan ortiq loyihalar, 9 yil xalqaro IT loyihalar bilan ishlash va $23 000 dollarlik resurs bitta kursda"/>
        <div class="marquee-wrapper">
          <div class="marquee">
            <Description class="text-block" varint="variant1" text="  UIC IT ACADEMY “ LEVEL UP ” " />
            <Description class="text-block" varint="variant1" text="  UIC IT ACADEMY “ LEVEL UP ” " />
            <Description class="text-block" varint="variant1" text="  UIC IT ACADEMY “ LEVEL UP ” " />
            <Description class="text-block" varint="variant1" text="  UIC IT ACADEMY “ LEVEL UP ” " />
            <Description class="text-block" varint="variant1" text="  UIC IT ACADEMY “ LEVEL UP ” " />
            <Description class="text-block" varint="variant1" text="  UIC IT ACADEMY “ LEVEL UP ” " />
          </div>
          <div>
            <h2 class="text-white text-[50px] font-bold translate-x-[180px] absolute translate-y-[-95px]">
             UIC IT ACADEMYDAN <span class="text-[50px] font-bold text-sky-500">“ LEVEL UP ”</span>  KURSI
            </h2>

            <p class="text-[20px] translate-x-[300px] text-center font-bold max-w-[700px] text-white">
              Kurs haqida batafsil ma'lumotga ega bo'lish uchun quyida ariza qoldiring!
            </p>
            
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import Description from "../Common/Description.vue";
  </script>
  
  <style scoped>
  .text {
    margin-bottom: 1rem; 
  }
  
  .marquee-wrapper {
    width: 100%;
    overflow: hidden;
    position: relative;
  }
  
  .marquee {
    display: flex;
    white-space: nowrap;
    animation: scroll 15s linear infinite;
  }
  
  @keyframes scroll {
    0% {
      transform: translateX(100%);
    }
    100% {
      transform: translateX(-100%);
    }
  }
  
  .text-block {
    display: inline-block;
    margin-right: 2rem;
  }
  </style>
  