<script setup>
definePageMeta({
  layout: "landing",
});
const { data: posts } = await useAsyncData('posts', () =>
  queryContent('/blog').sort({ date: -1 }).find()
)
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Welcome to the blog</template>
      <template v-slot:desc>Check out some cool posts:</template>
    </LandingSectionhead>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <NuxtLink
        v-for="post in posts"
        :key="post._path"
        :to="post._path"
        class="block border border-blue-200 rounded-lg bg-blue-50 p-4 hover:bg-blue-100 transition"
      >
        <h2 class="text-xl font-semibold mb-1">{{ post.title }}</h2>
        <p class="text-sm text-gray-600 mb-1">{{ post.description }}</p>
        <small class="text-xs text-gray-500">{{ post.date }}</small>
      </NuxtLink>
    </div>
      <!-- {
        team.map((item) => (
          <div class="group">
            <div class="w-full aspect-square">
              <Image
                {...item.avatar}
                format="avif"
                alt="Team"
                class="w-full h-full object-cover rounded transition  group-hover:-translate-y-1 group-hover:shadow-xl"
              />
            </div>

            <div class="mt-4 text-center">
              <h2 class="text-lg text-gray-800"> {item.name}</h2>
              <h3 class="text-sm text-slate-500"> {item.title}</h3>
            </div>
          </div>
        ))
      } -->

  </LandingContainer>
</template>
