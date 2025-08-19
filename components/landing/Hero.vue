<template>
  <main class="grid lg:grid-cols-2 place-items-center pt-16 pb-8 md:pt-8">
    <div class="p-24 hidden md:block">
      <img
        class="transition-tr\\wsl.localhost\Ubuntu-24.04ansform transform hover:scale-125"
        src="~/assets/img/nsardinia2.png"
        alt="Picture of Nicholas"
        loading="eager"
        format="avif"
        width="512"
        height="512"
      />
    </div>

    <div>
      <h1 class="text-5xl lg:text-6xl xl:text-5xl font-bold lg:tracking-tight">
        Nicholas Sardinia
      </h1>
      <p class="text-lg mt-4 text-slate-600 max-w-xl">
        an engineer passionate about building the future of technology.
        Check out my resume, portfolio, and development blog!
     </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink class="basis-2/3"
          href="https://drive.google.com/file/d/17nx8jHmY0HmkBwziam2i4q8pMoL-S63h/view?usp=sharing"
          target="_blank"
          rel="noopener"
          >Resume</LandingLink
        >
        <LandingLink class="basis-1/3"
          size="lg"
          styleName="outline"
          rel="noopener"
          href="/contact"
          target="_blank"
          >Contact</LandingLink
        >
      </div>
    </div>
  </main>
</template>
