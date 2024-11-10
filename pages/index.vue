<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import Header from '../components/header.vue'; 
import ScrolledHeader from '../components/ScrolledHeader.vue'; 
import AddToCart from '../components/addToCart.vue'; 

const hasScrolled = ref(false);
const isScrolled = ref(false);

// Handle scroll event to manage both header visibility and the sticky sidebar
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

// Add event listener for scroll on mount
onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

// Remove event listener for scroll on unmount
onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div class="flex flex-col">
    <!-- Floating Sidebar -->
    <div
      :class="{
        'fixed top-[20px]': isScrolled,
        'fixed top-[110px]': !isScrolled }"
      class="right-[80px] z-50 w-[28%] h-screen bg-white transition-all"
    >
      <AddToCart />
    </div>
  
    <!-- Header Change on Scroll -->
    <Header v-if="!hasScrolled" />
    <ScrolledHeader v-else />

    <!-- Main Content -->
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
