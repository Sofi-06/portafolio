<template>
  <section id="about" class="section">
    <div class="container">
      <div class="split-panel">
        <div class="portrait-card small">
          <div class="portrait-shape"></div>
          <img :src="profileImage" alt="Retrato personal" />
        </div>

        <div class="section-copy">
          <p class="eyebrow">Sobre mi</p>
          <h2 class="section-title left">Una mezcla de creatividad, detalle y ganas de aprender.</h2>
          <p class="section-text">
            Me gusta construir sitios que se sientan cercanos, limpios y bien
            pensados. Disfruto convertir ideas en interfaces visualmente
            atractivas, cuidando tanto la presentacion como la experiencia de
            uso.
          </p>

          <div class="stats-row">
            <article>
              <strong>HTML</strong>
              <span>Estructura clara</span>
            </article>
            <article>
              <strong>CSS</strong>
              <span>Diseno visual</span>
            </article>
            <article>
              <strong>Vue</strong>
              <span>Componentes reutilizables</span>
            </article>
          </div>

          <div class="skills soft">
            <span>JavaScript</span>
            <span>Git y GitHub</span>
            <span>Responsive Design</span>
            <span>UI basica</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import profileImage from '../assets/foto-perfil.png'
</script>
