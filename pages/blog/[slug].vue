<template>
  <LandingNavbar></LandingNavbar>
 <div class="max-w-3xl mx-auto px-6 py-10 prose prose-lg prose-gray">
    <article>
      <h1>{{ post.title }}</h1>
      <ContentRenderer :value="post" />
    </article>
  </div>
  <LandingFooter></LandingFooter>

  </template>

<script setup>
const { params } = useRoute()
const { data: post } = await useAsyncData(`post-${params.slug}`, () =>
  queryContent(`/blog/${params.slug}`).findOne()
)
console.log('POST', post.value)
</script>
