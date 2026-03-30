<template>
  <section id="projects" class="section">
    <div class="container">
      <div class="section-heading">
        <p class="eyebrow">Proyectos</p>
        <h2 class="section-title">Piezas que combinan diseno, estructura y experiencia.</h2>
      </div>

      <div class="projects-grid">
        <article class="project-card" v-for="project in projects" :key="project.title">
          <div class="project-visual" :class="project.accent">
            <span>{{ project.kicker }}</span>
            <strong>{{ project.title }}</strong>
          </div>

          <div class="project-content">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>

            <div class="tags">
              <span v-for="tech in project.tech" :key="tech">{{ tech }}</span>
            </div>

            <div class="links">
              <a :href="project.demo" target="_blank" rel="noreferrer">Demo</a>
              <a :href="project.deploy" target="_blank" rel="noreferrer">Deploy</a>
              <a :href="project.repo" target="_blank" rel="noreferrer">Repositorio</a>
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
    title: 'Landing de marca personal',
    kicker: 'UI Editorial',
    description: 'Propuesta visual con composicion suave, jerarquia clara y una presentacion enfocada en identidad.',
    accent: 'accent-rose',
    tech: ['Vue', 'CSS', 'JavaScript'],
    demo: 'https://youtube.com/',
    deploy: 'https://tu-deploy.com/',
    repo: 'https://github.com/tuusuario/proyecto1'
  },
  {
    title: 'Sitio de productos',
    kicker: 'Responsive',
    description: 'Proyecto pensado para destacar informacion y mantener una navegacion limpia en movil y escritorio.',
    accent: 'accent-cream',
    tech: ['Vue', 'HTML', 'CSS'],
    demo: 'https://youtube.com/',
    deploy: 'https://tu-deploy.com/',
    repo: 'https://github.com/tuusuario/proyecto2'
  },
  {
    title: 'Portafolio interactivo',
    kicker: 'Frontend',
    description: 'Interfaz enfocada en mostrar habilidades, proyectos y contacto con una experiencia visual consistente.',
    accent: 'accent-wine',
    tech: ['Vue', 'JavaScript', 'GitHub'],
    demo: 'https://youtube.com/',
    deploy: 'https://tu-deploy.com/',
    repo: 'https://github.com/tuusuario/proyecto3'
  }
]
</script>
