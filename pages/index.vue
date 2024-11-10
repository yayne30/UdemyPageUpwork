<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import Header from '../components/header.vue'; 
import ScrolledHeader from '../components/ScrolledHeader.vue'; 
import AddToCart from '../components/addToCart.vue'; 

const hasScrolled = ref(false);
const isScrolled = ref(false);

const handleScroll = () => {
  if (window.scrollY > 50) {
    hasScrolled.value = true;
  } else {
    hasScrolled.value = false;
  }

  if (window.scrollY > 0) {
    isScrolled.value = true;
  } else {
    isScrolled.value = false;
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div class="flex flex-col">
    <div
      :class="{
        'fixed top-[20px]': isScrolled,
        'fixed top-[110px]': !isScrolled }"
      class="right-[80px] z-50 w-[28%] h-screen bg-white transition-all"
    >
      <AddToCart />
    </div>
  
    <Header v-if="!hasScrolled" />
    <ScrolledHeader v-else />

    <Hero />
    <WhatLearn />
    <CourseInclude />
    <CourseContent />
    <Requirements />
    <StudentBoughtBox />
    <FrequentlyBought />
    <Instructor />
    <CourseRating />
    <MoreCourse />
    <Footer />
  </div>
</template>
