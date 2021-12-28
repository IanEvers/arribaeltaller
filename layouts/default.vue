<template>

  <v-app>
    <v-app-bar
      app
      color="white"
      flat
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="d-md-none"></v-app-bar-nav-icon>
      <v-img
          class="d-md-none centro"
          contain
          lazy-src="logoLEA.png"
          max-height="50"
          max-width="50"
          src="logoLEA.png"
      ></v-img>

      <v-img
          class="imagen d-none d-md-block"
          contain
          lazy-src="logoLEA.png"
          max-height="150"
          max-width="150"
          src="logoLEA.png"
      ></v-img>
      <v-navigation-drawer
        v-model="drawer"
        absolute
        left
        app
        temporary
      >
        <div class="linksSidebar">
          <NuxtLink v-for="link in links" :key="link.link" :to="link.link" v-bind:style="{color: link.color}">{{ link.nombre }}</NuxtLink>
        </div>

        <div class="flex-row row mt-1 mr-1">
          <v-btn
            icon
            v-for="red in redes" 
            :key="red.nombre"
            :color="red.color"
            class="color-inherit ms-1"
            :aria-label="red.nombre"
          >
            <a target="_blank" :href="red.url" class="inherit">
              <v-icon>mdi-{{red.nombre}}</v-icon>
            </a>
          </v-btn>
        </div>

      </v-navigation-drawer>

      <div class="links">
        <NuxtLink v-for="link in links" class="d-none d-md-block" :key="link.link" :to="link.link" v-bind:style="{color: link.color}">{{ link.nombre }}</NuxtLink>
      </div>

      <div class="flex-row">
        <v-btn
          icon
          v-for="red in redes" 
          :key="red.nombre"
          :color="red.color"
          :aria-label="red.nombre"
          class="ma-2 d-none d-md-block"
        >
          <a target="_blank" :href="red.url" class="inherit">
            <v-icon>mdi-{{red.nombre}}</v-icon>
          </a>
        </v-btn>
      </div>

    </v-app-bar>

    <v-main class="grey lighten-3">
      <v-container>
        <v-row>
          <Nuxt />
        </v-row>
      </v-container>
    </v-main>

    <v-footer
      color="#78cfe0"
      padless
    >
      <v-row
        justify="center"
        no-gutters
      >
      
        <v-col
          class="primary lighten-2 py-4 text-center white--text"
          cols="12"
        >
          {{ new Date().getFullYear() }} — <strong>Arriba el Taller</strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
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
      redes: [
        {
          nombre: 'email',
          url: 'mailto:leakletnicki@gmail.com',
          color: 'grey'
        },
        {
          nombre: 'facebook',
          url: 'https://www.facebook.com/Arriba-El-Taller-167016083381385',
          color: 'blue'
        },
        {
          nombre: 'instagram',
          url: 'https://www.instagram.com/arribaeltaller/',
          color: 'purple'
        },
        {
          nombre: 'youtube',
          url: 'https://www.youtube.com/channel/UCl63MEfTdIUynM7EeBngPrw',
          color: 'red'
        },
      ]
    }),
    head() {
      return {
        title: 'Arriba el Taller',
        meta: [
          {
            hid: 'Arriba el Taller  ',
            name: 'Arriba el Taller ',
            content: 'Arriba el Taller  .'
          }
        ]
      }
    }
  }
</script>

<style>
h2 {
  padding: 1rem;
  font-size: 3rem;
}

.row {
  justify-content: center;
}

a {
  text-decoration: none;
}

.inherit {
  color: inherit !important;
}

.theme--light.v-sheet{
  color: black;
}

.centro {
  display: contents;
}

.links {
  display: flex;
  gap: 2rem;
}

.linksSidebar {
  display: flex;
  flex-direction: column;
  padding: 1rem;
  gap: 1rem;
}

.v-toolbar__content {
  justify-content: space-evenly;
}

.v-image__image--preload {
  filter: none;
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


