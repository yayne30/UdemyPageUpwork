<script setup>
import { Icon } from "@iconify/vue";
import { ref, computed } from "vue";
</script>

<template>
  <div class="w-[56vw] ml-20 py-4 pr-44 mt-5 font-Zeitung">
    <h1 class="text-[20pt] font-extrabold">This Course Includes:</h1>
    <div  class="flex justify-between text-[12pt] pt-3">
       
    <div  class="flex gap-2 flex-col">
        
            <div class="flex gap-2 items-start">
          <Icon icon="material-symbols:live-tv-outline-sharp" width="20" />
          <h2>1.5 hours on-demand video</h2>
        </div>
        <div class="flex gap-2 items-start">
          <Icon icon="mdi:file-outline" width="20" />
          <h2>12 articles </h2>
        </div>

        </div>
        <div  class="flex gap-2 flex-col">
            <div class="flex gap-2 items-start">
          <Icon icon="fe:mobile" width="20" />
          <h2>Access on mobile and TV </h2>
        </div>
        <div class="flex gap-2 items-start">
          <Icon icon="hugeicons:champion" width="20" />
          <h2>Certificate of completion</h2>
        </div>

        </div>
    </div>

    
  </div>
  <div class="w-[56vw]  ml-20 pl-4 py-3 mt-10 font-Zeitung border-[1.2px] border-[#c1bfbf] flex flex-col gap-4">
    <div>
        <h1 class=" font-extrabold text-[13pt]">Top companies offer this course to their employees </h1>
    <p class="text-[#636262]">This course was selected for our collection of top-rated courses trusted by businesses worldwide. <a href="" class="text-[#6e40a3] underline">Learn More</a></p>
    </div>
    
   <div class="pr-5">
    <img src="../public/logosWhite.png"/>
   </div>
  </div>
</template>
