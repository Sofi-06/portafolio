<template>
  <section id="about" class="section">
    <div class="container">
      <div class="split-panel">
        <div class="about-aside">
          <div class="portrait-card small">
            <div class="portrait-shape"></div>
            <img :src="profileImage" alt="Retrato personal" />
          </div>

          <div class="stats-row about-highlights">
            <article class="reveal-up" style="--reveal-delay: 0ms">
              <strong>Comunicacion</strong>
              <span>Asertiva y clara al trabajar en equipo.</span>
            </article>
            <article class="reveal-up" style="--reveal-delay: 90ms">
              <strong>Trabajo en equipo</strong>
              <span>Colaboracion constante en proyectos y actividades.</span>
            </article>
            <article class="reveal-up" style="--reveal-delay: 180ms">
              <strong>Resolucion</strong>
              <span>Enfoque practico para analizar y resolver problemas.</span>
            </article>
            <article class="reveal-up" style="--reveal-delay: 270ms">
              <strong>Liderazgo</strong>
              <span>Iniciativa para organizar, proponer y aportar.</span>
            </article>
          </div>
        </div>

        <div class="section-copy">
          <p class="eyebrow">Sobre mi</p>
          <h2 class="section-title left">Construyo mi camino en desarrollo de software con curiosidad, disciplina y muchas ganas de seguir aprendiendo.</h2>
          <p class="section-text">
            Soy estudiante de Ingenieria de Sistemas con interes en el
            desarrollo de software, especialmente en backend y frontend. He
            participado en proyectos academicos enfocados en aplicaciones web,
            APIs y gestion de bases de datos, aplicando buenas practicas de
            programacion. Me caracterizo por la responsabilidad, el aprendizaje
            continuo y el trabajo en equipo, y busco seguir fortaleciendo mis
            habilidades tecnicas y adquirir experiencia profesional en el area
            de desarrollo de software.
          </p>

          <div class="skills soft about-languages">
            <span>HTML</span>
            <span>CSS</span>
            <span>JavaScript</span>
            <span>Java</span>
            <span>Python</span>
            <span>TypeScript</span>
            <span>MySQL</span>
            <span>PostgreSQL</span>
            <span>Spring Boot</span>
            <span>Git</span>
            <span>GitHub</span>
            <span>Vue</span>
          </div>

          <p class="about-support">
            Herramientas de apoyo: ChatGPT, Claude, GitHub Copilot y Lovable.
            Idiomas: Espanol nativo e ingles intermedio (B1).
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import profileImage from '../assets/foto-perfil.png'
</script>
