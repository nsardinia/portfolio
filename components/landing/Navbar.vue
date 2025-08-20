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
/* Pop + Fade animation */
.pop-fade-enter-active {
  transition: all 0.4s ease;
}
.pop-fade-leave-active {
  transition: all 0.3s ease;
}
.pop-fade-enter-from {
  opacity: 0;
  transform: scale(0.95);
}
.pop-fade-enter-to {
  opacity: 1;
  transform: scale(1);
}
.pop-fade-leave-from {
  opacity: 1;
  transform: scale(1);
}
.pop-fade-leave-to {
  opacity: 0;
  transform: scale(0.95);
}
</style>

<template>
  <LandingContainer>
  <div class="flex mt-4 hidden lg:flex">
    <div class="flex-1">
      <nav class="h-full">
        <ul class="flex items-center h-full space-x-6">
        <li class="flex-1 max-w-24">
          <a href="/" 
             class="relative font-bold text-lg text-gray-800 hover:text-purple-700 transition">
            <span class="after:content-[''] after:absolute after:left-0 after:-bottom-1 
                         after:w-0 after:h-[2px] after:bg-purple-700 
                         after:transition-all after:duration-300 
                         hover:after:w-full">
              Home
            </span>
          </a>
        </li>

        <li class="flex-1 max-w-24">
          <a href="contact" 
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
          <a href="portfolio" 
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
          <a href="blogIndex" 
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
  <!--
  <div class="flex lg:hidden relative">
  <div class="flex">
    <button @click="isOpen = !isOpen" class="p-2 text-gray-800 focus:outline-none">
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"/>
      </svg>
    </button>
    </div>
      </div>
    <transition name="pop-fade">
      <div 
        v-if="isOpen" 
        class="fixed inset-0 bg-black/90 flex flex-col justify-center items-center space-y-8 z-40"
      >
        <a href="#home" class="text-white text-2xl font-semibold hover:underline">Home</a>
        <a href="#about" class="text-white text-2xl font-semibold hover:underline">About</a>
        <a href="#projects" class="text-white text-2xl font-semibold hover:underline">Projects</a>
        <a href="#articles" class="text-white text-2xl font-semibold hover:underline">Articles</a>

        <div class="flex space-x-6 pt-8">
          <a href="#"><i class="fab fa-twitter text-2xl text-white hover:text-blue-400"></i></a>
          <a href="#"><i class="fab fa-github text-2xl text-white hover:text-gray-300"></i></a>
          <a href="#"><i class="fab fa-linkedin text-2xl text-white hover:text-blue-500"></i></a>
          <a href="#"><i class="fab fa-pinterest text-2xl text-white hover:text-red-500"></i></a>
          <a href="#"><i class="fab fa-dribbble text-2xl text-white hover:text-pink-400"></i></a>
        </div>
      </div>
    </transition> -->
<div class="block lg:hidden">
    <!-- Hamburger / Close button -->
    <div class="flex mr-2">
      <button @click="isOpen = !isOpen" class="p-2 text-gray-800 focus:outline-none relative z-50 flex-1">
        <svg v-if="!isOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
        <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M6 18L18 6M6 6l12 12"/>
        </svg>
      </button>
        <div class="flex-1 justify-center mt-4">
            <span class="inline-flex h-16 w-16 items-center justify-center rounded-full 
                     bg-black text-white font-extrabold text-2xl 
                     transition-colors duration-300 hover:bg-purple-700">
                  NS
            </span>
        </div>
      <div>
        <button @click="isOpen = !isOpen" class="p-2 text-gray-800 focus:outline-none relative z-50 mt-5">
        <svg v-if="!isOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
        <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M6 18L18 6M6 6l12 12"/>
        </svg>
      </button>
      </div>
    </div>


    <!-- Fullscreen Mobile Menu -->
    <transition name="pop-fade">
      <div 
        v-if="isOpen" 
        class="fixed inset-0 bg-black/90 flex flex-col justify-center items-center space-y-8 z-40 m-10 mt-24 rounded-xl"
      >
        <a href="/" class="text-white text-2xl font-semibold hover:underline">Home</a>
        <a href="contact" class="text-white text-2xl font-semibold hover:underline">Contact</a>
        <a href="portfolio" class="text-white text-2xl font-semibold hover:underline">Portfolio</a>
        <a href="blog" class="text-white text-2xl font-semibold hover:underline">Blog</a>

        <!-- Social icons row -->
        <div class="flex space-x-6 pt-8">
          <a target="_blank" href="https://instagram.com/nicholassardinia"><i class="fab fa-instagram text-2xl text-white hover:text-blue-400"></i></a>
          <a target="_blank" href="https://www.github.com/nsardinia"><i class="fab fa-github text-2xl text-white hover:text-gray-300"></i></a>
          <a target="_blank" href="https://www.linkedin.com/in/nsardinia"><i class="fab fa-linkedin text-2xl text-white hover:text-blue-500"></i></a>
        </div>
      </div>
    </transition>
  </div>


  </LandingContainer>
</template>
