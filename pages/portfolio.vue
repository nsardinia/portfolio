<script setup>
definePageMeta({
  layout: "landing",
});
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Projects</template>
      <template v-slot:desc>Here's what I've been working on</template>
    </LandingSectionhead>
    <div class="mt-4 text-center">
      (Coming soon! For now, check out my github page) 
    </div>
    <div class="text-center">
    <p class="mt-2">
      Hacker3D
    </p>
    <p class="mt-2">
      RoboMZ3 
    </p>
    <p class="mt-2">
      FlexiCare
      </p>
      <p class="mt-2">
      VibeNotes
      </p>
      <p class="mt-2">
      Bathydrone
      </p>
      <p class="mt-2">
      SubjuGator
      </p>
      <p class="mt-2">
      Combat Robotics
      </p>
      <p class="mt-2">
      .
      </p>
      <p class="mt-2">
      .
      </p>
      <p class="mt-2">
      .
      </p>       
      <p class="mt-2">
      Teams and Orgs: UF-MIL, APRILab, Gator Battlebots
      </p>
       
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
