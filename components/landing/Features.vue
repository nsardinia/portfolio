<script setup>
const features = [
  {
    title: "Python",
  },
  {
    title: "C/C++",
  },
  {
    title: "Java",
  },
  {
    title: "JavaScript",
  },
  {
    title: "Docker",
  },
  {
    title: "Vue",
  },
  {
    title: "PyTorch",
  }, 
  {
    title: "Pandas",
  },
  {
    title: "ExpressJS",
  },

];
</script>

<template>
  <div class="mt-16 md:mt-0">
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      Skills
    </h2>
    <p class="text-lg mt-4 text-slate-600">
      I have a uniqe knowledge set and a strong passion for learning.
    </p>
  </div>
  <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">
    <div v-for="item of features" class="justify-center flex gap-4 items-start">
      <div>
        <h3 class="font-semibold text-lg">{{ item.title }}</h3>
      </div>
    </div>
  </div>
</template>
