<script setup>
const menuitems = [
  {
    title: "Portfolio",
    path: "/portfolio",
  },
  {
    title: "Contact",
    path: "/contact",
  },
  {
    title: "Blog",
    path: "/blogIndex",
  },

]

const isOpen = ref(false);
</script>

<style>
/* Simple slide-down + fade animation */
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.2s ease;
}
.slide-fade-enter-from {
  opacity: 0;
  transform: translateY(-10px);
}
.slide-fade-enter-to {
  opacity: 1;
  transform: translateY(0);
}
.slide-fade-leave-from {
  opacity: 1;
  transform: translateY(0);
}
.slide-fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>

<template>
  <LandingContainer>
  <div class="flex mt-4 hidden lg:flex">
    <div class="flex-1">
      <nav class="h-full">
        <ul class="flex items-center h-full space-x-6">
        <li class="flex-1 max-w-24">
          <a href="#contact" 
             class="relative font-bold text-lg text-gray-800 hover:text-purple-700 transition">
            <span class="after:content-[''] after:absolute after:left-0 after:-bottom-1 
                         after:w-0 after:h-[2px] after:bg-purple-700 
                         after:transition-all after:duration-300 
                         hover:after:w-full">
              Contact
            </span>
          </a>
        </li>
        <li class="flex-1 max-w-24">
          <a href="#portfolio" 
             class="relative font-bold text-lg text-gray-800 hover:text-purple-700 transition">
            <span class="after:content-[''] after:absolute after:left-0 after:-bottom-1 
                         after:w-0 after:h-[2px] after:bg-purple-700 
                         after:transition-all after:duration-300 
                         hover:after:w-full">
              Portfolio
            </span>
          </a>
        </li>
        <li class="flex-1 max-w-24">
          <a href="#blog" 
             class="relative font-bold text-lg text-gray-800 hover:text-purple-700 transition">
            <span class="after:content-[''] after:absolute after:left-0 after:-bottom-1 
                         after:w-0 after:h-[2px] after:bg-purple-700 
                         after:transition-all after:duration-300 
                         hover:after:w-full">
              Blog
            </span>
          </a>
        </li>
      </ul>
    </nav>    
    </div>
    <div class="flex-1">
      <div class="flex justify-center">
        <div>
          <span class="inline-flex h-16 w-16 items-center justify-center rounded-full 
             bg-black text-white font-extrabold text-2xl 
             transition-colors duration-300 hover:bg-purple-700">
          NS
          </span>
        </div>
      </div>
    </div>
    <div class="flex-1">

  <nav class="h-full">
    <ul class="flex items-center justify-end h-full space-x-6">
      <!-- LinkedIn -->
      <li>
        <a href="https://www.linkedin.com/in/nsardinia" target="_blank" rel="noopener noreferrer"
           class="transition-transform transform hover:scale-110">
          <img src="/assets/icons/64px-LinkedIn_icon.svg.png" alt="LinkedIn"
               class="w-6 h-6 object-contain" />
        </a>
      </li>

      <!-- GitHub -->
      <li>
        <a href="https://github.com/nsardinia" target="_blank" rel="noopener noreferrer"
           class="transition-transform transform hover:scale-110">
          <img src="/assets/icons/128px-Octicons-mark-github.svg.png" alt="GitHub"
               class="w-6 h-6 object-contain" />
        </a>
      </li>

      <!-- Instagram -->
      <li>
        <a href="https://instagram.com/nicholassardinia" target="_blank" rel="noopener noreferrer"
           class="transition-transform transform hover:scale-110">
          <img src="/assets/icons/128px-Instagram_logo_2022.svg.png" alt="Instagram"
               class="w-6 h-6 object-contain" />
        </a>
      </li>
    </ul>
  </nav>
    </div>
  </div> 
  <div class="block lg:hidden relative">
    <!-- Hamburger button -->
    <button @click="isOpen = !isOpen" class="p-2 text-gray-800 focus:outline-none">
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"/>
      </svg>
    </button>

    <!-- Mobile menu -->
    <transition name="slide-fade">
      <div 
        v-if="isOpen" 
        class="mt-4 w-full bg-white p-4 shadow-lg rounded-lg flex flex-col items-center space-y-4"
      >
        <a href="#contact" class="text-lg font-bold text-gray-800 hover:text-blue-600">Contact</a>
        <a href="#portfolio" class="text-lg font-bold text-gray-800 hover:text-blue-600">Portfolio</a>
        <a href="#blog" class="text-lg font-bold text-gray-800 hover:text-blue-600">Blog</a>
      </div>
    </transition>
  </div>  
  </LandingContainer>
</template>
