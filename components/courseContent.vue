<script setup>
import { Icon } from "@iconify/vue";
import { ref } from "vue";

const sections = ref([
  {
    title: "Welcome",
    lectures: 5,
    length: "15m",
    expanded: false,
    content: [
      "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "A Serious Look at Fun & Games",
    lectures: 10,
    length: "15m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "Design Thinking for instructional design",
    lectures: 1,
    length: "76m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "GAME MECHANIC #1: Points & Scoring",
    lectures: 3,
    length: "45m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "GAME MECHANIC #2: Badging",
    lectures: 9,
    length: "60m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "GAME MECHANIC #3: Randomization",
    lectures: 3,
    length: "45m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "GAME MECHANIC #4: Competiton & Cooperation",
    lectures: 1,
    length: "50m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "GAME MECHANIC #5: Roleplay & Simulation",
    lectures: 6,
    length: "13m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "Game mechanic lighting round: 25+ more mechanics",
    lectures: 5,
    length: "35m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
  {
    title: "Reflection & ending the game",
    lectures: 6,
    length: "87m",
    expanded: false,
    content: [
    "Laying out the game board",
      "Getting Started",
      "How to access activities",
      "ACTIVITY: Getting started",
      "Lecture 5: First Steps",
    ],
  },
]);

const toggleSection = (index) => {
  sections.value[index].expanded = !sections.value[index].expanded;
};
</script>

<template>
  <div class="w-[70vw] ml-20 py-4 pr-44 mt-5 font-Zeitung">
    <h1 class="text-[18pt] font-extrabold">Course Content</h1>
    <div class="mt-5 w-full">
      <div class="flex justify-between">
        <p>10 sections • 27 lectures • 1h 30m total length</p>
      </div>
      <div class="mt-4">
        <div 
          v-for="(section, index) in sections" 
          :key="index" 
          class="border-[1px] border-gray-200"
        >
          <div 
            class="flex justify-between items-center cursor-pointer p-3 bg-[#f7fbfc]" 
            @click="toggleSection(index)"
          >
            <div class="flex items-center">
              <Icon 
                :icon="section.expanded ? 'mdi:chevron-up' : 'mdi:chevron-down'" 
                width="20" height="20" 
                class="mr-2" 
              />
              <h2 class="text-[12.5pt] font-semibold">{{ section.title }}</h2>
            </div>
            <p class="text-sm">{{ section.lectures }} lectures • {{ section.length }}</p>
          </div>

        
          <div 
            v-if="section.expanded" 
            class="p-4  text-gray-700"
          >
            <ul class="">
                <div >
                    
                    <div class="flex justify-between" v-for="(lecture, lectureIndex) in section.content" :key="lectureIndex">
                        <div class="flex gap-4 ">
                            <Icon icon="material-symbols:live-tv-outline-sharp" width="20" />
                            {{ lecture }}
                        </div>
                 <div class="flex gap-5">
                    <a class="text-[#1f2aa1] underline"> Preview </a>
                    <p>03:41</p>

                 </div>
                    
                    </div>
                    

                </div>
              
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Optional styles for better presentation */
</style>
