<template>
  <section class="hero-shell">
    <div class="container">
      <div class="hero-card">
        <div class="hero-copy">
          <p class="eyebrow">Portafolio creativo</p>
          <h1>
            Diseno experiencias web con una estetica suave, moderna y muy
            cuidada.
          </h1>
          <p class="hero-description">
            Soy estudiante y desarrolladora en formacion. Me enfoco en crear
            interfaces agradables, funcionales y con una identidad visual que
            haga memorable cada proyecto.
          </p>

          <div class="hero-actions">
            <a href="#projects" class="btn btn-primary">Ver proyectos</a>
            <a href="#contact" class="btn btn-secondary">Hablemos</a>
          </div>

          <div class="hero-metrics">
            <article>
              <strong>3+</strong>
              <span>Proyectos visuales</span>
            </article>
            <article>
              <strong>6</strong>
              <span>Tecnologias base</span>
            </article>
            <article>
              <strong>100%</strong>
              <span>Enfoque responsivo</span>
            </article>
          </div>
        </div>

        <div class="hero-visual">
          <div class="hero-photo-frame">
            <div class="hero-photo-blob"></div>
            <img :src="profileImage" alt="Foto de perfil" />
            <span class="hero-orbit orbit-one"></span>
            <span class="hero-orbit orbit-two"></span>
          </div>

          <div class="hero-floating-card">
            <p>Diseno UI</p>
            <strong>Landing pages, portafolios y experiencias web claras.</strong>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import profileImage from '../assets/foto-perfil.png'
</script>
