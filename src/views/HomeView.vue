<template>
  <v-app style="overflow-x: hidden;">
    <v-app-bar app color="primary" dark flat>
      <v-toolbar-title class="font-weight-bold">CLIMORA</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn text to="#sobre" class="d-none d-md-flex">Sobre</v-btn>
      <v-btn text to="#downloads" class="d-none d-md-flex">Downloads</v-btn>
      <v-btn text to="#video" class="d-none d-md-flex">Vídeo</v-btn>
      <v-btn text to="#link" class="d-none d-md-flex">Link</v-btn>

      <v-app-bar-nav-icon class="d-flex d-md-none" @click="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app temporary color="primary" location="right" dark
    >
      <v-list>
        <v-list-item link @click="drawer = false" to="#sobre">
          <v-list-item-title>Sobre</v-list-item-title>
        </v-list-item>
        <v-list-item link @click="drawer = false" to="#downloads">
          <v-list-item-title>Downloads</v-list-item-title>
        </v-list-item>
        <v-list-item link @click="drawer = false" to="#video">
          <v-list-item-title>Vídeo</v-list-item-title>
        </v-list-item>
        <v-list-item link @click="drawer = false" to="#link">
          <v-list-item-title>Link</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <div class="d-sm-flex align-center justify-center">
        <div class="pa-0">
          <img src="../assets/logo.png" max-width="320" class="mx-auto"/>
        </div>
        <div id="sobre" class="py-16 text-center w-sm-50">
          <h1 class="text-h3 font-weight-bold mb-4">Conheça o CLIMORA</h1>
          <p class="text-body-1 mb-6">
            O CLIMORA une tecnologia, colaboração e dados da NASA para oferecer previsões
            meteorológicas em tempo real, combinadas com relatos reais de usuários.
            Uma nova forma de compreender e compartilhar o clima.
          </p>
        </div>
      </div>
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

      <v-container id="video" class="py-16 text-center">
        <h2 class="text-h4 font-weight-bold mb-4">Assista ao Vídeo do Pitch</h2>
        <div class="d-flex justify-center">
          <iframe width="560" height="315" src="https://www.youtube.com/embed/L_0PwTfDW-A" title="CLIMORA - Pitch" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
          </iframe>
        </div>
      </v-container>


      <v-container id="link" class="py-16 text-center grey lighten-4">
        <h2 class="text-h4 font-weight-bold mb-4">Saiba Mais</h2>
        <p class="text-body-1 mb-6">
          Descubra mais sobre o CLIMORA e como estamos transformando a forma de entender o clima.
        </p>
        <v-btn color="primary" size="large" href="https://seusite.com" target="_blank" rounded elevation="4">
          Acesse o APP oficial
        </v-btn>
      </v-container>
    </v-main>

    <v-footer color="primary" dark padless>
      <v-col class="text-center py-4">
        © {{ new Date().getFullYear() }} Equipe BMG — CLIMORA 🚀
      </v-col>
    </v-footer>
  </v-app>
</template>

<script setup lang="ts">
  import { ref } from 'vue';
  const drawer = ref(false)

</script>

<style>

.d-none {
  display: none !important;
}
.d-flex {
  display: flex !important;
}
.d-md-flex {
  display: none !important; 
}

@media (min-width: 960px) {
  .d-md-flex {
    display: flex !important; 
  }
  .d-md-none {
    display: none !important; 
  }
}
</style>