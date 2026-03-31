<template>
  <div class="page-shell">
    <Navbar />
    <Hero />
    <About />
    <Projects />
    <Footer />
  </div>
</template>

<script setup>
import { nextTick, onBeforeUnmount, onMounted } from 'vue'
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Footer from './components/Footer.vue'

let revealObserver

onMounted(async () => {
  await nextTick()

  const revealItems = document.querySelectorAll('.reveal-up')

  revealObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible')
          return
        }

        entry.target.classList.remove('is-visible')
      })
    },
    {
      threshold: 0.16,
      rootMargin: '0px 0px -8% 0px'
    }
  )

  revealItems.forEach((item) => revealObserver.observe(item))
})

onBeforeUnmount(() => {
  revealObserver?.disconnect()
})
</script>
