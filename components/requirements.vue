<script setup>
import { Icon } from "@iconify/vue";
import { ref } from 'vue';

const showFullText = ref(false);
</script>

<template>
  <div class="w-[56vw] ml-20 py-3 mt-5 font-Zeitung flex flex-col gap-2">
    <h1 class="text-[17pt] font-extrabold">Requirements</h1>
    <div>
        <ul class="list-disc ml-3">
            <li>Basic understanding of course design</li>
            <li>Everyday supplies to prototype solutions (paper, Post-Its, pens, markers, tape, etc.)</li>
        </ul>
    </div>
    <h1 class="text-[17pt] mt-3 font-extrabold">Description</h1>
    <h2 class="font-extrabold mb-4">Ready to change the game?</h2>

    <p class="text-[11pt]">
      <span v-if="showFullText">
        If you've missed one of our popular gamification classes at Stanford, here's your chance to learn about <strong>gamification for training & learning.</strong> In this new course, you'll learn how to analyze popular games for the elements that make them work, make them fun, and make them perfect for your learning challenges.
        <br><br>
        In this <strong>highly interactive workshop</strong>, you'll play, design, and test more than 10 unique game mechanics – giving you an insider's view into how to incorporate them into your next learning challenge.
        <br><br>
        You'll also have the opportunity to apply your learning to up to <strong>5 distinct learning challenges</strong> that you're facing now, giving you a <strong>jumpstart on applying your learning</strong> in the real world.
        <br><br>
        We also believe that fun is a key driver for learning – so we'll have a lot of it along the way. This isn't a boring "death by PowerPoint" course. Get ready to <strong>roll up your sleeves</strong> and <strong>get gaming</strong>.
        <br><br>
        Finally, we'll share <strong>success stories</strong> (and a couple of failures) about how we've specifically incorporated games into our practice at some of the world's most recognized brands.
        <br><br>
        <strong class="text-[17pt]">Who this course is for:</strong>
        <ul class="list-disc ml-10">
          <li>Instructional designers, teachers, & professionals looking to create more engaging courses</li>
          <li>HR professionals hoping to make meetings and workshops more interesting</li>
          <li>Managers & leaders who want to have more fun with team activities & off-site strategy planning sessions</li>
          <li>Anyone interested in game design for learning & change</li>
        </ul>
      </span>
      
      <span v-else>
        If you've missed one of our popular gamification classes at Stanford, here's your chance to learn about <strong>gamification for training & learning.</strong> In this new course, you'll learn how to analyze popular games for the elements that make them work, make them fun, and make them perfect for your learning challenges...
        <br><br>
        In this <strong>highly interactive workshop</strong>, you'll play, design, and test more than 10 unique game mechanics – giving you an insider's view into how to incorporate them into your next learning challenge.
        <br><br>
        You'll also have the opportunity to apply your learning to up to <strong>5 distinct learning challenges</strong> that you're facing now, giving you a <strong>jumpstart on applying your learning</strong> in the real world.
        <br><br>
      </span>
    </p>

    <!-- Show More / Show Less Button with Arrow Icons -->
    <button @click="showFullText = !showFullText" class="mt-2 text-[#4e1774] font-extrabold hover:underline self-start flex items-center gap-1">
      <Icon :icon="showFullText ? 'akar-icons:chevron-up' : 'akar-icons:chevron-down'" width="15" height="15" />
      {{ showFullText ? 'Show less' : 'Show more' }}
    </button>
  </div>
</template>
