<script>
export default {
    name: 'MenuComponent',
    methods: {
    mostrarAlerta() {
      alert('¡Me alegra que te guste!');
    }
  }
};


</script>

<template>
    <div class="menu">
        <div class="fondo-codigo glitch-fondo"></div>
        <h1 class="titulo glitch-texto">🚨 hay apoyo, solo falta talento 🚨</h1>
        <div class="foto-con-marco">
          <img src="https://avatars.githubusercontent.com/u/108552455?v=4" alt="mi foto" class="foto-perfil alternativa">
        </div>
        <p class="descripcion parpadeo">
          Soy Nico.<br>
          Me gusta diseñar webs divertidas.<br>
          Aprendiz y apasionado del frontend. <s>que se pudra el backend</s><br>
          Creyente del margin negativo.<br>
          Objetivos: <br>
          - Centrar un div <br>
          - Borrar una base de datos <br>
          - Conseguir trabajo de frontend <br>
        </p>
        <h2>Te gusta la pagina?</h2>
        <br>
        <div class="likes">
          <button class="btn dislike" @click="mostrarAlerta">👎 Dislike</button>
          <button class="btn like" @click="mostrarAlerta">👍 Like</button>
        </div>
    </div>
</template>
