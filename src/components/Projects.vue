<template>
  <section id="projects" class="section">
    <div class="container">
      <h2 class="section-title">Mis proyectos</h2>

      <div class="projects-grid">
        <article class="project-card" v-for="project in projects" :key="project.title">
          <img :src="project.image" :alt="project.title" />
          
          <div class="project-content">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>

            <div class="tags">
              <span v-for="tech in project.tech" :key="tech">{{ tech }}</span>
            </div>

            <div class="links">
              <a :href="project.demo" target="_blank">Demo</a>
              <a :href="project.deploy" target="_blank">Deploy</a>
              <a :href="project.repo" target="_blank">Repositorio</a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: 'Proyecto 1',
    description: 'Aplicación web enfocada en una experiencia visual clara, moderna y responsiva.',
    image: '/src/assets/proyecto1.png',
    tech: ['Vue', 'CSS', 'JavaScript'],
    demo: 'https://youtube.com/',
    deploy: 'https://tu-deploy.com/',
    repo: 'https://github.com/tuusuario/proyecto1'
  },
  {
    title: 'Proyecto 2',
    description: 'Proyecto desarrollado para organizar contenido y mostrar información de forma atractiva.',
    image: '/src/assets/proyecto2.png',
    tech: ['Vue', 'HTML', 'CSS'],
    demo: 'https://youtube.com/',
    deploy: 'https://tu-deploy.com/',
    repo: 'https://github.com/tuusuario/proyecto2'
  },
  {
    title: 'Proyecto 3',
    description: 'Sitio web con estructura limpia y funcionalidades enfocadas en la experiencia del usuario.',
    image: '/src/assets/proyecto3.png',
    tech: ['Vue', 'JavaScript', 'GitHub'],
    demo: 'https://youtube.com/',
    deploy: 'https://tu-deploy.com/',
    repo: 'https://github.com/tuusuario/proyecto3'
  }
]
</script>