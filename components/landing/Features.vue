<script setup>
const features = [
  {
    title: "Python",
    icon: "bx:bxs-briefcase",
  },
  {
    title: "C/C++",
    icon: "bx:bxs-window-alt",
  },
  {
    title: "Java",
    icon: "bx:bxs-data",
  },
  {
    title: "JavaScript",
    icon: "bx:bxs-bot",
  },
  {
    title: "Docker",
    icon: "bx:bxs-file-find",
  },
  {
    title: "Vue",
    icon: "bx:bxs-user",
  },
];
</script>

<template>
  <div class="mt-16 md:mt-0">
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      Skills
    </h2>
    <p class="text-lg mt-4 text-slate-600">
      A uniqe knowledge set and a strong passion for learning.
    </p>
  </div>

  <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">
    <div v-for="item of features" class="flex gap-4 items-start">
      <div class="mt-1 bg-black rounded-full p-2 w-8 h-8 shrink-0">
        <Icon class="text-white" :name="item.icon" />
      </div>
      <div>
        <h3 class="font-semibold text-lg">{{ item.title }}</h3>
        <p class="text-slate-500 mt-2 leading-relaxed">
          {{ item.description }}
        </p>
      </div>
    </div>
  </div>
</template>
