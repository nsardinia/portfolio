<template>
  <article>
    <h1>{{ post.title }}</h1>
    <ContentRenderer :value="post" />
    <p>Slug: {{ $route.params.slug }}</p>
  </article>
</template>

<script setup>
const { params } = useRoute()
const { data: post } = await useAsyncData(`post-${params.slug}`, () =>
  queryContent(`/blog/${params.slug}`).findOne()
)
console.log('POST', post.value)
</script>
