<script setup>
import { Icon } from '@iconify/vue';
</script>

<template>
  <header class="w-screen fixed mt-3 h-max flex items-center font-Montserrat ">
    <nav class="flex  items-center justify-between px-6">
        <div class="flex items-center">
            <NuxtLink to="/"> <img src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy.svg" class="w-[91px] h-[34px]"alt="Logo" />  </NuxtLink>
            <a class="my-3 px-3 text-[10pt] font-bold hover:text-[#5e4bbd]">Categories</a>
        </div>
        <div class="mx-3 w-[470px] h-12 rounded-3xl border-[1px] border-black relative flex items-center bg-[rgb(243,246,249)]">
  <Icon icon="mdi:magnify" width="25" class="absolute left-4 text-gray-500"></Icon>
  <input 
    type="text" 
    
    class="rounded-3xl h-full w-full outline-none pl-12 text-[10pt] placeholder:text-[#3f3d3d] bg-transparent placeholder" 
    placeholder="Search for anything" 
  />
</div>

      <div class="flex text-[10pt] font-semibold ">
        <NuxtLink class="px-3 hover:text-[#5e4bbd]" >Udemy Business</NuxtLink>
        <NuxtLink class="px-3 hover:text-[#5e4bbd]" >Teach on Udemy</NuxtLink>
        <NuxtLink class="px-3 hover:text-[#5e4bbd]"> <Icon icon="material-symbols:shopping-cart-outline-rounded" width="25"></Icon></NuxtLink>

        
      </div>

      <div class="flex gap-2">
      <button class="px-3 border-[1.3px] h-10 w-20 text-[10pt] border-black font-extrabold hover:bg-slate-200" > Log in </button>
      <button class="px-3  h-10 w-20 text-[10pt] text-white bg-black font-extrabold hover:bg-slate-700" > Sign Up</button>
      <button class="px-[9px] border-[1.3px] h-10 w-10 py-[9px] border-black hover:bg-slate-200"">
  <Icon icon="solar:global-linear" width="20"></Icon>
      </button>
     
    </div>
    </nav>
  </header>
</template>
