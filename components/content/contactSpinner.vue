<template>
  <!-- Floating Hire Me widget -->
  <div
    class="fixed z-50 flex items-center justify-center
           top-4 right-4
           w-24 h-24 md:w-48 md:h-48
           md:bottom-4 md:left-4 md:top-auto md:right-auto"
  >
    <div
      class="relative w-full h-full flex items-center justify-center group"
    >
      <!-- Rotating circular text image -->
      <img 
        src="/assets/img/inkpx-curved-text.png" 
        alt="Circular Text"
        class="absolute inset-0 w-12/12 h-12/12 animate-spin-slow 
               group-hover:opacity-80 transition pointer-events-none m-auto"
      />

      <!-- Hire Me Button -->
      <a
        href="mailto:nicholas_sardinia@outlook.com?subject=Hiring%20Inquiry&body=Hi%20Nicholas%2C%0D%0A%0D%0AI'd%20like%20to%20discuss%20a%20project%20with%20you."
        class="w-3/5 h-3/5 rounded-full bg-gray-900 flex items-center justify-center 
               text-white text-xs md:text-base lg:text-xl font-bold transition-colors duration-300 
               group-hover:bg-white group-hover:text-gray-900
               group-hover:border-2 group-hover:border-gray-900
               shadow-lg"
      >
        Hire Me
      </a>
    </div>
  </div>
</template>

<script setup>
// no logic needed
</script>

<style scoped>
@keyframes spin-slow {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
.animate-spin-slow {
  animation: spin-slow 20s linear infinite;
}
</style>
