<template>
  <v-app>
    <!-- HEADER -->
    <v-app-bar app color="primary" dark flat>
      <v-toolbar-title class="font-weight-bold">🌤 CLIMORA</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text to="#sobre">Sobre</v-btn>
      <v-btn text to="#downloads">Downloads</v-btn>
      <v-btn text to="#video">Vídeo</v-btn>
      <v-btn text to="#link">Link</v-btn>
    </v-app-bar>

    <!-- BODY -->
    <v-main>
      <!-- Seção 1: Introdução -->
      <v-container id="sobre" class="py-16 text-center">
        <h1 class="text-h3 font-weight-bold mb-4">Conheça o CLIMORA</h1>
        <p class="text-body-1 mb-6">
          O CLIMORA une tecnologia, colaboração e dados da NASA para oferecer previsões
          meteorológicas em tempo real, combinadas com relatos reais de usuários.
          Uma nova forma de compreender e compartilhar o clima.
        </p>
        <v-img
          src=""
          max-width="320"
          class="mx-auto rounded-xl elevation-3"
        />
      </v-container>

      <!-- Seção 2: Downloads -->
      <v-container id="downloads" class="py-16 text-center grey lighten-4">
        <h2 class="text-h4 font-weight-bold mb-4">Baixe e Explore</h2>
        <p class="text-body-1 mb-6">
          Faça o download da versão web, acesse os previews ou veja o app em ação.
        </p>
        <v-row justify="center" class="gap-4">
          <v-btn color="primary" size="large">Download Web</v-btn>
          <v-btn color="secondary" size="large">Preview Mobile</v-btn>
        </v-row>
      </v-container>

      <!-- Seção 3: Vídeo -->
      <v-container id="video" class="py-16 text-center">
        <h2 class="text-h4 font-weight-bold mb-4">Assista ao Vídeo do Projeto</h2>
        <div class="d-flex justify-center">
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/SEU_VIDEO_AQUI"
            title="CLIMORA - Pitch"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
      </v-container>

      <!-- Seção 4: Link externo -->
      <v-container id="link" class="py-16 text-center grey lighten-4">
        <h2 class="text-h4 font-weight-bold mb-4">Saiba Mais</h2>
        <p class="text-body-1 mb-6">
          Descubra mais sobre o CLIMORA e como estamos transformando a forma de entender o clima.
        </p>
        <v-btn
          color="primary"
          size="large"
          href="https://seusite.com"
          target="_blank"
          rounded
          elevation="4"
        >
          🌍 Acesse o site oficial
        </v-btn>
      </v-container>
    </v-main>

    <!-- FOOTER -->
    <v-footer color="primary" dark padless>
      <v-col class="text-center py-4">
        © {{ new Date().getFullYear() }} Equipe BMG — Projeto CLIMORA 🚀
      </v-col>
    </v-footer>
  </v-app>
</template>

<script setup lang="ts">
// Nenhum script necessário por enquanto
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
</style>
