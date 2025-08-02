---
title: How it's made | tech blog edition. 
description: VueJS, Nuxt, Digital Ocean, Nuxt-Content
date: 2025-07-27
layout: blog
thumbnail: /images/screenshot-2025-07-27-202019.png
---

A few months ago, I decided to update my old personal website, <https://nsardinia.com/>, with something that was a bit more powerful and could showcase my portfolio a bit better. I wanted to move away from a static site, and towards something more extensible, especially if I ever wanted to write some applets into the page itself.

I used a Vue / Vite / Express stack at my internship in Fall '24, and enjoyed working with Vue, so I decided to rewrite the site that way. I also wanted to try SSR (really, really not necessary for this page and doing this means I might need to rewrite it again someday, but here we are) so I found the Nuxt framework and built up a skeleton. . .

<img src="/images/screenshot-2025-07-27-202424.png" alt="Description" style="max-width: 600px; width: 100%; height: auto; display: block; margin: 0 auto;" />

Not too exciting, but it does the job.

With this done, I just had to implement the blog functionality, which was relatively simple using nuxt-content, a git-based CMS for nuxt projects. <https://content.nuxt.com/>

After playing around with the documentation a bit, I came to something like this:

<img src="/images/screenshot-2025-07-27-202019.png" alt="Description" style="max-width: 600px; width: 100%; height: auto; display: block; margin: 0 auto;" />

The most barebones of barebones implementations, but it's fast and comes with an editor tool (nuxt studio) that I'm using to write this very post. Pretty cool!

All that was left is to update my digitalocean droplet and restart pm2 (more on this coming soon, once I automate things with github actions), and . . . yep, the changes are live, probably where you're reading this right now! Feel free to fork the repo and built up a simple blog of your own ;) 

Thanks for reading,

\- Nick
