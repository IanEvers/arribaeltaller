<template>
      <v-col
        cols="16"
        sm="12"
    >
        <v-sheet
            rounded="lg"
        >
            <h2 class="actividades"> Actividades </h2>

            <p >Esta es una pequeña guía para realizar producciones. Son sólo sugerencias para inspirar, pueden modificarlas, transformarlas, mezclarlas, y todo, todo lo que se les ocurra hacer con ellas.
                No hay ningún resultado al que llegar, sólo disfrutar del proceso y estar atentos a lo que vaya surgiendo en el camino. Es un mapa para que ustedes decidan por dónde ir, si es que necesitan un mapa.
                Nos encantaría ver sus obras y si nos dan permiso las publicamos. 
                Si quieren seguir trabajando o buscar inspiración, pueden buscar en nuestras redes más propuestas.
                ¡Y ahora Manos a la Obra!
            </p>

            <v-tabs
                v-model="tab"
                background-color="transparent"
                center-active
                grow
                show-arrows
            >
                <v-tab
                    v-for="actividad in actividades"
                    :key="actividad.nombre"
                >
                    {{ actividad.nombre }}
                </v-tab>
                </v-tabs>

                <v-tabs-items v-model="tab">
                <v-tab-item
                    v-for="actividad in actividades"
                    :key="actividad.nombre"
                >
                    <v-card
                        color="basil"
                        flat
                    >
                    <p>{{ actividad.texto }}</p>
                    </v-card>
                </v-tab-item>
                </v-tabs-items>
        </v-sheet>
    </v-col>
</template>
<script>
export default {
    data () {
        return {
            tab: null,
            actividades: [
                {
                    nombre:'Tu propio Museo',
                    texto: 'Vas a diseñar tu museo en miniatura. Materiales: 1 caja, cartones, papeles, tijera, pegamento, lo que quieras y necesites para dibujar, pintar y construir. A trabajar!  Dentro de la caja vas a pensar un recorrido, cuál sería la entrada, también podrías agregar paredes con cartón, tal vez puedas hacer un baño, un bar, una tienda, la boletería y ¡por supuesto tus obras en miniatura! Pueden ser dibujos, pinturas, esculturas, y todo lo que quieras. ¡es tu museo! Una vez que finalices tus obras, probá dónde iría cada una y cuando lo definas ya las podés ir pegando dentro de tu museo. ',
                },
                {
                    nombre: 'En movimiento',
                    texto: `Crearemos un dibujo con movimiento
                      Materiales:
                      2 hojas, tijera, 1 palito (puede ser de helado, de brochette o una ramita no muy frágil) cinta o
                      pegamento, lo que quieras para dibujar y pintar.
                      A trabajar!
                      En una hoja dibujamos un paisaje (playa, montañas, ciudad, selva etc) o cualquier lugar (negocio,
                      una habitación, etc). Lo pintamos. En otra hoja dibujamos algún objeto o animal o personaje que
                      elijamos para que se mueva en nuestro paisaje. Por ejemplo, si dibujé una ciudad, podría ser un
                      auto que vaya por una calle, o si dibujé una selva, podría ser un mono que vaya de un árbol a
                      otro, etc. lo pintamos, lo recortamos y le pegamos el palito del lado de atrás del dibujo
                      (En esta parte tal vez tengamos que pedir ayuda a algún adulto)
                      Tomamos nuestro paisaje y vamos a pensar como queremos que se mueva nuestro objeto, animal o
                      personaje y vamos a trazar una línea, es importante que no llegue al borde de la hoja y recortamos
                      por ahí. Luego pasamos el palito (objeto o animal o personaje) por el corte y lo movemos desde
                      atrás).`,

                },
                {
                    nombre:'Almohadón de papel',
                    texto: `  Materiales
                      1 hoja grande, papel de diario, o revista, o papel higiénico, si están con un adulto abrochadora y si no, cinta o pegamento, tijera y lo que quieran para dibujar y pintar.
                      A trabajar!
                      Doblar la hoja por la mitad (punta con punta) y dibujar en uno de sus lados un objeto o animal o personaje lo más grande posible. Pintar. Luego con mucho cuidado recortar el dibujo, con la hoja de abajo al mismo tiempo, de tal manera que me queden las 2 hojas iguales. En la segunda hoja vamos a dibujar a ese objeto o animal o personaje de espalda o del lado de atrás. Pintamos las dos hojas. Cuando terminamos, vamos hacer bollitos de papel de diario, revista o higiénico y vamos apoyarlos del lado de atrás de uno de los dibujos (}. Luego lo cubrimos con el otro dibujo, cuando nos queda el dibujo “inflado” como una almohada lo cerramos con abrochadora, cinta o pegamento. Fíjense si cuando van cerrando tienen que hacer más bollitos de papel o si tienen que sacar para que no se rompa el papel.                      `,
                },
                {
                    nombre:'La silla',
                    texto: `  Trabajo inspirado en la pintura de Vincent Van Gogh.
                      Vincent Van Gogh, fue un artista diferente para su época y por eso fue un artista reconocido mucho
                      tiempo después de su muerte. Tal vez conozcas sus famosos “girasoles” o un maravilloso cuadro “la
                      noche estrellada”. Te proponemos trabajar a partir de un cuadro no tan conocido. Si podés busca en
                      internet el cuadro de este artista llamado “Silla” y la observes. Cuál es el objeto principal, ves
                      otros objetos, a quién pertenece la silla, cómo te diste cuenta?
                      Te despierta algún sentimiento cuando observas este cuadro? Por qué?
                      Cómo es la pincelada, qué colores usa?
                      Y ahora te toca a vos
                      Materiales
                      Una hoja, tijera, lo que quieras para dibujar y pintar
                      A trabajar!
                      Doblamos la hoja a la mitad (punta con punta). Sobre el lado que doblamos (la parte cerrada)
                      dibujamos dos líneas paralelas de unos 3, 4 cm. Puede ser en el medio o de costado. Luego abrimos
                      la hoja, y con el dedo empujamos el corte de tal manera que nos quede un asiento. Y ahora vamos a
                      convertirla en una silla que nos guste. Vamos a imaginar dónde está nuestra silla, en un
                      restaurant, en un living, en un jardín? Donde nos guste! Y lo vamos a dibujar y pintar.
`,
                },
                {
                    nombre:'Arte abstracto',
                    texto: ` Escuchar colores, pintar la música
                      A principios del siglo 20, Wassily Kandinsky, de pequeño, fue a un concierto. Y mientras sonaba la
                      música, comenzó a ver colores, luego en su casa tomó sus acuarelas y mientras pintaba empezó a
                      escuchar la música de cada color, (por eso muchas de sus obras se llaman Composiciones, podés
                      buscarlas en internet). Este fue el nacimiento del Arte Abstracto.
                      Actividad
                      Materiales
                      Reproductor de música, varias hojas, lo que quieras para pintar.
                      A trabajar!
                      Te proponemos que pongas canciones con diferentes estilos de música en tu reproductor y con cada
                      una vayas dibujando lo que sientas, con diferentes colores, distintos tipos de líneas y formas.
                      Por ejemplo, en una canción de cuna, ¿Cómo son las líneas, largas, onduladas, qué colores usaste?,
                      y con una canción de rock? se cortan? Son finas o gruesas? tienen puntas?
                      Podés hacer una obra por cada canción o varias en una misma hoja.
                      También, si querés, seguilas con otros dibujos y otros materiales.`
                },
               
                {
                    nombre:'Arte abstracto II',
                    texto: ` Podés mirar obras de arte abstracto (Kandinsky, Ad Reinhardt, Miró, etc).
                      Materiales
                      1 hoja, marcador negro, y lo que quieras para dibujar y pintar.
                      A trabajar!
                      Doblamos la hoja libremente todas las veces que podamos. La abrimos y observamos las líneas que se
                      formaron y con el marcador negro las remarcamos. A partir de ahí comenzamos a crear como más nos
                      guste, tal vez entre las líneas reconocemos un objeto o animal o personaje y lo queremos dibujar,
                      agregar detalles y pintar, o llenamos cada forma con un color o con una textura visual diferente
                      en cada uno; también podemos transformarlo en un collage y agregar otros materiales.`,
                },
            
            ],
        }
    },
}
</script>

<style scoped>

.actividades {
    color: #1A4E90;
}
</style>