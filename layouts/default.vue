<template>

  <v-app id="inspire">
    <v-app-bar
      app
      color="white"
      flat
      
    >

    <v-img
        class="d-sm-none"
        contain
        lazy-src="logoLEA.png"
        max-height="50"
        max-width="50"
        src="logoLEA.png"
    ></v-img>

    <v-img
        class="imagen d-none d-sm-block"
        contain
        lazy-src="logoLEA.png"
        max-height="150"
        max-width="150"
        src="logoLEA.png"
    ></v-img>

    <NuxtLink v-for="link in links" class="d-none d-sm-block"
        :key="link.link" :to="link.link" v-bind:style="{color: link.color}">{{ link.nombre }}</NuxtLink>          

    </v-app-bar>

    <v-main class="grey lighten-3">
      <v-container>
        <v-row>
            <Nuxt />
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      isActive: false,
      links: [
        {
          nombre: 'Nuestro Proyecto',
          link: '/',
          color: 'green'
        },
        {
          nombre: 'Nuestro Espacio',
          link: 'nuestroEspacio',
          color: '#8B1470'
        },
        {
          nombre: 'Galería',
          link: 'galeria',
          color: '#ff5733'
        },
        {
          nombre: 'Lxs chicxs dicen',
          link: 'lxsChicxsDicen',
          color: '#8B6CA1'
        },
        {
          nombre: 'Actividades',
          link: 'actividades',
          color: '#1A4E90'
        },
        {
          nombre: '20 años',
          link: '20anos',
          color: '#808000'
        },
      ],
    }),
  }
</script>

<style>
.row {
    justify-content: center;
}

a {
    text-decoration: none;
}

.v-toolbar__content {
    justify-content: space-evenly;
}

.imagen {
    margin-top: 5rem;
}

.v-lazy {
    display: contents;
}
.col-sm-12 {
    padding: 0;
}
</style>


