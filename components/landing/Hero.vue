<template>
  <main class="grid lg:grid-cols-2 place-items-center pt-16 pb-8 md:pt-8">
    <div class="p-24 md:order-1 hidden md:block">
      <img
        class="rounded-full transition-transform transform hover:scale-125"
        src="~/assets/img/nsardinia.jpeg"
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
        I'm an engineer passionate about building the future of technology.
        Check out my resume, portfolio, and development blog!
     </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink
          href="https://drive.google.com/file/d/17nx8jHmY0HmkBwziam2i4q8pMoL-S63h/view?usp=sharing"
          target="_blank"
          rel="noopener"
          >Resume</LandingLink
        >
        <LandingLink
          size="lg"
          styleName="outline"
          rel="noopener"
          href="/portfolio"
          target="_blank"
          >Portfolio</LandingLink
        >
        <LandingLink
          size="lg"
          styleName="outline"
          rel="noopener"
          href="/blogIndex"
          target="_blank"
          >Blog</LandingLink
        >
      </div>
    </div>
  </main>
</template>
