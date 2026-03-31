<template>
  <section id="projects" class="section">
    <div class="container">
      <div class="section-heading">
        <p class="eyebrow">Proyectos</p>
        <h2 class="section-title projects-title">Una seleccion de trabajos donde he puesto en practica mis habilidades.</h2>
      </div>

      <div class="projects-grid">
        <article
          class="project-card reveal-up"
          v-for="(project, index) in projects"
          :key="project.title"
          :style="{ '--reveal-delay': `${index * 90}ms` }"
        >
          <div class="project-visual" :class="[project.accent, { 'has-image': project.image }]">
            <img
              v-if="project.image"
              class="project-shot"
              :src="project.image"
              :alt="project.imageAlt"
            />

            <div class="project-overlay">
              <span>{{ project.kicker }}</span>
              <strong>{{ project.title }}</strong>
              <small>{{ project.label }}</small>
            </div>
          </div>

          <div class="project-content">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>

            <div class="tags">
              <span v-for="tech in project.tech" :key="tech">{{ tech }}</span>
            </div>

            <div class="links">
              <a
                v-for="link in project.links"
                :key="link.url"
                :href="link.url"
                :class="['link-pill', `link-${link.kind}`]"
                target="_blank"
                rel="noreferrer"
              >
                {{ link.label }}
              </a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
import inventarioImage from '../assets/Captura de pantalla 2026-03-31 090817.png'
import creditRiskImage from '../assets/Captura de pantalla 2026-03-31 090830.png'
import startupConnectImage from '../assets/Captura de pantalla 2026-03-31 090842.png'
import trackUImage from '../assets/Captura de pantalla 2026-03-31 090854.png'

const projects = [
  {
    title: 'Pagina CV',
    kicker: 'Sitio personal',
    label: 'Presentacion profesional',
    description: 'Pagina web tipo hoja de vida pensada para presentar perfil, habilidades, experiencia academica y canales de contacto en una interfaz clara.',
    accent: 'accent-rose',
    tech: ['HTML', 'CSS', 'JavaScript', 'UI Web'],
    links: [
      {
        label: 'Repositorio',
        url: 'https://github.com/Sofi-06/pagina-cv',
        kind: 'repo'
      }
    ]
  },
  {
    title: 'Hora Nomina',
    kicker: 'Gestion academica',
    label: 'Registro y seguimiento',
    description: 'Aplicacion para registrar horas, organizar evidencias y apoyar procesos de nomina docente con formularios, autenticacion y consulta de informacion.',
    accent: 'accent-cream',
    tech: ['Angular', 'FastAPI', 'MySQL', 'JWT', 'Python'],
    links: [
      {
        label: 'Repositorio',
        url: 'https://github.com/Sofi-06/hora-nomina',
        kind: 'repo'
      }
    ]
  },
  {
    title: 'CreditRiskAI',
    kicker: 'IA aplicada',
    label: 'Scoring crediticio',
    description: 'Sistema de scoring crediticio con machine learning que integra XGBoost, clustering con HDBSCAN y explicabilidad mediante SHAP.',
    accent: 'accent-wine',
    tech: ['Python', 'XGBoost', 'SHAP', 'TIMi Suite'],
    image: creditRiskImage,
    imageAlt: 'Vista del formulario del proyecto CreditRiskAI',
    links: [
      {
        label: 'Video',
        url: 'https://youtu.be/OgJDpXkAldY?si=BDYZ8JPtem00W1xh',
        kind: 'video'
      },
      {
        label: 'Repositorio',
        url: 'https://github.com/Sofi-06/creditRiskAI',
        kind: 'repo'
      }
    ]
  },
  {
    title: 'StartUpConnect',
    kicker: 'Ecosistema emprendedor',
    label: 'Incubacion de startups',
    description: 'Sistema web para gestionar el ciclo de vida de startups, con seguimiento del MVP, acompanamiento estrategico y apoyo a la financiacion.',
    accent: 'accent-cream',
    tech: ['Java', 'Spring Boot', 'Web App', 'Gestion'],
    image: startupConnectImage,
    imageAlt: 'Vista principal de la plataforma StartUpConnect',
    links: [
      {
        label: 'Video',
        url: 'https://youtu.be/atWDRnqNnvY?si=MF0eiK9sjAyE1Vcq',
        kind: 'video'
      },
      {
        label: 'Repositorio',
        url: 'https://github.com/danimorenocr/StartUpConnect',
        kind: 'repo'
      }
    ]
  },
  {
    title: 'TrackU',
    kicker: 'Seguimiento academico',
    label: 'Trabajos de grado',
    description: 'Sistema para gestionar el proceso de trabajos de grado y facilitar el seguimiento entre estudiantes, docentes y evaluadores.',
    accent: 'accent-wine',
    tech: ['HTML', 'CSS', 'JavaScript', 'Gestion'],
    image: trackUImage,
    imageAlt: 'Panel de usuario del proyecto TrackU',
    links: [
      {
        label: 'Video',
        url: 'https://youtu.be/dxjKGDJSztk?si=R45I7-px1kCDwj-9',
        kind: 'video'
      },
      {
        label: 'Repositorio',
        url: 'https://github.com/Sofi-06/TrackU-Project',
        kind: 'repo'
      }
    ]
  },
  {
    title: 'Inventario',
    kicker: 'Control de recursos',
    label: 'Gestion de laboratorio',
    description: 'Aplicacion web para inventarios de laboratorio que automatiza procesos manuales, centraliza la informacion y mejora el control de recursos.',
    accent: 'accent-rose',
    tech: ['Java', 'Inventario', 'Laboratorio', 'Backend'],
    image: inventarioImage,
    imageAlt: 'Pantalla de acceso del sistema de inventario',
    links: [
      {
        label: 'Video',
        url: 'https://youtu.be/asCaU3KpJIQ?si=Sk1r1jETCQi2SDuW',
        kind: 'video'
      },
      {
        label: 'Repositorio',
        url: 'https://github.com/Sofi-06/Inventario',
        kind: 'repo'
      }
    ]
  }
]
</script>
