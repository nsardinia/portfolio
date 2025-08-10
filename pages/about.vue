<script setup>
definePageMeta({
  layout: "landing",
});
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Nicholas Sardinia</template>
      <template v-slot:desc>Engineer, Developer, Innovator</template>
    </LandingSectionhead>

    <div class="grid md:grid-cols-1 gap-10 mx-auto max-w-4xl mt-16">
      <div>
        <p class="text-lg text-left leading-relaxed text-slate-500 mt-3">
        Here's a brief into to me, my journey, and the skills I've developed. 
        </p>
        <p class="text-lg text-left leading-relaxed text-slate-500 mt-3">
        Here's how to get in touch with me professionally.
        </p>
      </div>
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
