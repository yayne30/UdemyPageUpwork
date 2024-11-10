<script setup>
import { Icon } from '@iconify/vue';
import { ref, computed } from 'vue';

// Array of students with their details
const students = [
  { id: 1, imageSrc: "../public/students.png", name: "Design Thinking for Beginners: Develop Innovative Ideas", teacher:"Laura Pickel", rating: "4.4", reviews: "126,180", price: "$89.99" },
  { id: 2, imageSrc: "../public/students.png", name: "Creative Problem Solving", rating: "4.6", teacher:"Laura Pickel",reviews: "126,180", price: "$89.99",  },
  { id: 3, imageSrc: "../public/students.png", name: "Innovative Thinking Techniques",teacher:"Laura Pickel", rating: "4.3",reviews: "126,180",  price: "$89.99" },
  
];


</script>
<template>
    <div class="w-[56vw] ml-20 px-5 py-4 mt-10 font-Zeitung border-[1.2px] border-[#ababab]">
      <h1 class="text-[20pt] font-extrabold">Frequently Bought Together</h1>
      
      <div class="grid grid-cols-1 gap-4 w-[100%]">
        <div v-for="student in students" :key="student.id" class="grid grid-cols-[2fr,5fr] gap-2 py-[5px] items-center w-full">
          
          <div class="h-[110px] w-[220px]">
            <img src="../public/students.png" alt="student-image" class="w-full h-full object-cover" />
          </div>
          
          <div class="flex flex-col gap-1">
            <div class="flex justify-between items-center">
              <span class="font-extrabold text-[13pt] w-[70%]">{{ student.name }}</span>
              <span class="text-[14pt] font-extrabold">{{ student.price }}</span>
            </div>
            
            <div class="flex text-gray-900 gap-1 text-[12pt]">
              <span class="font-normal">{{ student.teacher }}</span>
            </div>
  
            <div class="flex items-center font-normal text-[11pt]">
              <span class="font-extrabold">{{ student.rating }}</span>
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <Icon icon="ri:star-s-fill" class="text-yellow-500" />
              <span>({{ student.reviews }})</span>
            </div>
          </div>
          
        </div>
      </div>
      <div class="flex justify-between items-center mt-2">
        <h1 class="text-[15pt]"> Total: <strong>$184.97</strong></h1>
        <button class="bg-purple-800 p-3 text-white font-extrabold text-[12pt]">Add all to cart</button>
      </div>
    </div>
  </template>
  