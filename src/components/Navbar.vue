<template>
  <header class="navbar">
    <div class="container nav-content">
      <a href="#" class="logo" aria-label="Inicio">
        <img :src="logoImage" alt="Logo del portafolio" class="logo-image" />
        <span class="logo-title">MiPortafolio</span>
      </a>

      <nav>
        <a href="#about">Sobre mi</a>
        <a href="#projects">Proyectos</a>
        <a href="#contact">Contacto</a>
      </nav>
    </div>
  </header>
</template>

<script setup>
import logoImage from '../assets/SLOGO.png'
</script>
