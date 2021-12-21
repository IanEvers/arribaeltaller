<template>
  
    <v-col
      cols="16"
      sm="12"
    >
      <v-sheet>
        <div class="contenedorEstrellas">

          <v-img
            class="imagenMapa"
            src="MapaLea.png" 
            max-height="85vh"
            contain
          > </v-img>

          <v-btn
            v-for="tarjeta in tarjetas"
            v-bind:key="tarjeta.id"
            fab
            small
            :color="tarjeta.color"
            class="ma-2 boton d-none d-md-block elevation-1 floating"
            @click="tarjeta.dialog = !tarjeta.dialog"
            :style="'left:' + tarjeta.posicion.left + '; top:' + tarjeta.posicion.top"
          >
            <v-icon>mdi-star</v-icon>
          </v-btn>

          <v-dialog
            v-for="tarjeta in tarjetas"
            v-bind:key="tarjeta.titulo"
            v-model="tarjeta.dialog"
            max-width="800px"
          >
            <v-card class="ov-none" :style="'border: 10px solid '+tarjeta.color">
              <div class="flex-row">
                <div class="mb-2">

                  <v-img
                    class="imagenFondo"
                    width="275"
                    :src="tarjeta.contenido.fondo"
                  ></v-img>

                  <v-img
                    class="ma-3 imagenCard"
                    height="250"
                    width="250"
                    :src="tarjeta.contenido.imagen"
                  ></v-img>
                </div>

                <div>

                  <v-card-title>
                    <span>{{tarjeta.contenido.titulo}}</span>
                    <v-spacer></v-spacer>
                  </v-card-title>
                  
                  <v-card-text>
                    <div class="text--primary lg" v-html="tarjeta.contenido.texto"> </div>
                  </v-card-text>

                </div>

              </div>
                <div class="flex-center">
                <v-card-actions>

                <v-btn
                  color="primary"
                  text
                  
                  @click="tarjeta.dialog = false"
                >
                  Cerrar
                </v-btn>
                </v-card-actions>
              </div>
            </v-card>
          </v-dialog>
        </div>

        <v-img
          src="imaginarYcrear.jpeg"
        ></v-img>

        <h2 class="verde">Nuestro Proyecto</h2>

        <p>Construir en la arena… 
          <br>
          <br>
          Dibujar en un vidrio empañado…
          <br>
          <br>
          Desde muy pequeñxs tenemos el impulso de dejar huellas, de crear formas y experimentar. Crear imágenes es una necesidad, desde los comienzos de la historia y esto permanece a lo largo de toda la vida.
          <br>
          <br>
          Nos interesa el arte como forma de conocimiento, el arte como forma de vida, de una vida feliz.
          <br>
          <br>
          El arte se parece mucho al juego, es el mismo proceso. Quizás la única diferencia entre arte y juego sea que en el arte la producción se “ve” y perdura. 
          <br>
          <br>
          Al igual que en el juego, con la expresión plástica lxs chicxs nos proporcionan una parte de sí mismos. Cómo piensan, sienten y ven.
          <br>
          <br>
          Para eso en el taller lxs ayudamos a encontrar los temas, los materiales y técnicas más convenientes para que puedan expresarse.
          <br>
          <br>
           Es decir que a medida que van trabajando en su producción van adquiriendo tanto elementos del lenguaje plástico, como la utilización de materiales y herramientas.
          <br>
          <br>
          El taller es la posibilidad de aprender haciendo, de potenciar los conocimientos y adquirir nuevos saberes para expresar las ideas propias, estar atentxs a los descubrimientos y abiertxs a las posibilidades, animarse a lo diferente. 
          <br>
          <br>
          Sumando la emoción como forma de adquirir conocimiento: Dibujamos, pintamos, construimos aquello que nos despierte un sentimiento, una emoción. Con la expresión plástica se “dicen” cosas que no se podrían decir de otra manera. 
          <br>
          <br>
          Todo comienza con las ganas: ganas de usar materiales y herramientas que permitan expresar ideas y sentimientos personales a través del lenguaje plástico.
          <br>
          <br>
          En el taller trabajamos en grupos por edades pero la propuesta es que cada unx pueda elegir. Muchxs llegan con alguna idea o tema de lo que quieren hacer y entonces comienza el diálogo:
          <br>
          <br>
          -Quiero hacer una jirafa.
          <br>
          - ¿La querés dibujar o construir?
          <br>
          - Construir
          <br>
          - Muy bien, ¿y qué materiales te parece que podemos usar? ¿Cartón, arcilla, maderas, material de desecho?
          <br>
          Otros llegan sabiendo el material que quieren usar y entonces el diálogo gira en torno al tema para desplegar con el material que eligieron.
          <br>
          -Quiero usar maderas
          <br>
          - ¿Y qué vas hacer con las maderas?
          <br>
          <br>
          Y están lxs que llegan sin saber qué van a hacer, entonces, para ellxs tenemos reservada la "cajita de las ideas".
          <br>
          <br>
          En el taller se genera un clima de fiesta y alegría. Un clima dónde todos estamos ocupados en una actividad placentera. 
          <br>
          <br>
          Buscamos ampliar la experiencia de lxs chicxs para su actividad creadora. Acompañamos el trabajo sin interferir en su creatividad.
          <br>
          <br>
          El espacio está disponible para ellos. Materiales al alcance y a la vista. Las posibilidades crecen. Lxs chicxs crean en libertad. Respetamos sus elecciones.
          <br>
          <br>
          Lxs chicxs en el taller saben que su actividad creadora es importante y valorada por el adulto. Confiamos en lxs chicxs y sus decisiones.
          <br>
          <br>
          Lxs adultxs estamos “disponibles” para escuchar, para ayudar, para proveer materiales, para compartir saberes. Transmitimos alegría por” hacer” expresivamente. 
          <br>
          <br>
          Cada tanto, hacemos propuestas que seguramente no conozcan y puedan así ampliar sus posibilidades expresivas, como hacer papeles florentinos, máscaras (usando de molde su propia cara), esgrafiados, pinturas en movimiento, libros de artista, movibles de madera, dibujos a partir de la silueta de su cuerpo, talla en piedra, murales.
          <br>
          <br>
          También les ofrecemos actividades especiales que constituyen la esencia del taller como "La Noche del Taller", las salidas a Museos y Galerías y las muestras de fin de año. En el taller lxs chicxs pueden tener hasta tres trabajos empezados. Respetamos sus tiempos. Como artistas sabemos que a veces un trabajo necesita “descansar” y luego se retoma, se profundiza, y se termina.
          <br>
          <br>
          “Todo niño es un artista. El problema es cómo mantenerse siéndolo una vez que se ha crecido”
          <br>
          Pablo Picasso
        </p>

        <v-img
          contain
          class="imagenGrande"
          src="proyecto.jpeg"
          max-height="90vh"
        ></v-img>
      </v-sheet>
    </v-col>
</template>

<script>

export default {
  data () {
    return {
      tarjetas: [
        {
          id: 1,
          dialog: false,
          color: '#C4A433',
          posicion: {
            top: '80%',
            left: '50%'
          },
          contenido: {
            fondo: '1 Noche del taller/01 fondo.png',
            imagen: '1 Noche del taller/01 foto tarj.png',
            titulo:  ` Noche del taller `,
            texto: `
              Es el ritual que se repite año tras año; en vacaciones de invierno y verano. Un ritual que es el mismo pero nunca igual. 
              <br>
              <br>
              Llegar al taller cuando cae la noche, con linterna, bolsas de dormir, pijamas, cepillos de dientes y porque no, algún muñeco y un libro para leer antes de dormir. La emoción y la alegría va aumentando con cada una de las actividades, pintar con flúo y luz negra, derretir crayones en una vela, hacer dibujos con luz, dibujar la sombra del perfil del amigo o amiga que se proyecta en la pared. Siempre realizamos alguna actividad nueva para sorprenderlos.
              <br>
              <br>
              También, claro, cenar y …dormir en el taller!
              <br>
              <br>
              La mini Noche del Taller
              <br>
              <br>
              Los más chicos del taller también querían vivir la experiencia. Sin quedarse a dormir y con las propuestas nocturnas adaptadas a su edad, ell@s también tuvieron su Mini Noche de Taller.`,
          },
        },
        {
          id: 2,
          dialog: false,
          color: '#4056BF',
          posicion: {
            top: '25%',
            left: '30%'
          },
          contenido: {
            fondo: '2 Murales/02 fondo.png',
            imagen: '2 Murales/02 foto tarj.png',
            titulo:  ` Murales `,
            texto: `
              En 2010, "Arriba el Taller" propuso la realización de un mural en las paredes del patio de la biblioteca La Nube (Jorge Newbery 3537, caba). El mural fue diseñado y pintado por los chicos y chicas que ese año asistían al taller. Esta experiencia les permitió el abordaje de una experiencia única y disfrutar de una creación grupal. 
              <br>
              <br>
              Para la inauguración del mural realizamos un evento junto a la muestra anual de producciones realizadas por los chicos en el taller.
              <br>
              <br>
              Después de la experiencia en La Nube el entusiasmo continuó y entonces pintamos las paredes del baño del taller y cuando ya no quedaba ningún huequito continuamos con la puerta
              <br>
              <br>
              En 2019 iniciamos una nueva propuesta. Un mural grupal en las paredes de nuestra terraza. Pintamos unos árboles/plantas y cada unx de lxs chicxs del taller que quisiera participar tendría que hacer una flor de cerámica. Es maravilloso ver este mural que no para de crecer, que además de flores tiene plantas, abejas y bichitos de luz. Continuará…
            `,
          },
        },
        {
          id: 3,
          dialog: false,
          color: '#7DCF2A',
          posicion: {
            top: '20%',
            left: '50%'
          },
          contenido: {
            fondo: '3 La Terraza/03 fondo.png',
            imagen: '3 La Terraza/03 foto tarj.png',
            titulo:  `La Terraza`,
            texto: ` Es parte de nuestro espacio creativo. A veces funciona como extensión del taller en los días templados, entonces sacamos mesas y sillas o simplemente apoyamos en el piso, sobre todo si son proyectos muy grandes y a veces ese piso es parte de algunas obras con tizas.`,
          },
        },
        {
          id: 4,
          dialog: false,
          color: '#C0C0C0',
          posicion: {
            top: '60%',
            left: '80%'
          },
          contenido: {
            fondo: '4 Festejo de los 10 años/04 fondo.png',
            imagen: '4 Festejo de los 10 años/04 foto tarj.png',
            titulo:  ` Festejo de los 10 años`,
            texto: `En marzo de 2012, el museo Saavedra nos abrió sus puertas para que realicemos nuestra fiesta. En ese maravilloso contexto fue el reencuentro con alumn@s que pasaron por el taller, también exponiendo alguna obra que crearon en el taller en algún momento y además las de los alumn@s que asistían al taller en ese momento. A la muestra, sumamos un recorrido histórico a través de fotografías, recuerdos y objetos que pertenecen al taller. También disfrutamos de diferentes actividades de las que realizamos habitualmente en el taller y otras aprovechando el espacio. `,
          },
        },
        {
          id: 5,
          dialog: false,
          color: '#05C9F5',
          posicion: {
            top: '90%',
            left: '30%'
          },
          contenido: {
            fondo: '5 Mascaras/05 fondo.png',
            imagen: '5 Mascaras/05 foto tarj.png',
            titulo:  `Máscaras `,
            texto: `L@s chic@s amasan y estiran la arcilla, se sientan cómodos, cierran los ojos y la boca y se colocan la “plancha” de arcilla sobre su cara y mientras la sostienen con sus manos lo más cerca posible de las orejas, los maestros buscamos la nariz y marcamos la forma, luego marcamos los ojos, labios y mentón. Después la sacamos lentamente y la apoyamos en un “colchón” de diarios envueltos en una bolsa para que permanezca la forma redondeada de la cabeza y no se aplane.
            <br>
            <br>
            Sobre esto l@s chic@s empiezan a crear; para algun@s será un autorretrato, para otr@s algún conocido y para otr@s un personaje inventado. Pero todos van a observar y construir las diferentes partes del rostro, completar ojos y boca, orejas, cejas y el pelo, algunos le agregarán barba, bigotes, anteojos, aros, hebillas, vinchas. Cuando está lista, al igual que los otros trabajos de arcilla, lo dejamos secar bien para llevarlo al horno de cerámica. Cuando sale, se esmalta o sea le damos color y ahí l@s chic@s eligen si la piel es clara u oscura, el color de los ojos y el pelo. `,
          },
        },
        {
          id: 6,
          dialog: false,
          color: '#73EFFB',
          posicion: {
            top: '15%',
            left: '60%'
          },
          contenido: {
            fondo: '6 Muestras/06 fondo.png',
            imagen: '6 Muestras/06 foto tarj.png',
            titulo:  `Muestras `,
            texto: ` Es la muestra de l@s chic@s. Es por eso que participar es su elección tanto como las producciones que se van a exhibir. Ponemos un número límite máximo de obras para que tod@s tengan la misma oportunidad. Lo ideal es hacer el montaje a la altura promedio de los ojos de los chic@s, ya que en los museos y galerías se toma en cuenta la de los adultos, pero como son tantos trabajos no siempre lo logramos. Somos conscientes de lo que moviliza ver la obra colgada en una muestra, fuera del taller y fuera de las casas. Es importante también, como parte del proceso. Es en este momento, cuando hay espectador que le da sentido, cuando se cierra el círculo y la producción se convierte en obra de arte. 
            <br>
            <br>
            Los últimos años elegimos para exponer un centro cultural cercano al taller, El Laberinto de Chas, porque es un espacio que queremos mucho, nos dan absoluta libertad y además es de fácil acceso para tod@s. El evento dura un día y allí nos reunimos con l@s chicxs, sus familias y amig@s, realizamos alguna actividad que tod@s puedan participar y luego repartimos algún regalo del taller en agradecimiento por el momento  y el año compartido. `,
          },
        },
        {
          id: 7,
          dialog: false,
          color: '#0B7015',
          posicion: {
            top: '20%',
            left: '40%'
          },
          contenido: {
            fondo: '7 Regalos/07 fondo.png',
            imagen: '7 Regalos/07 foto tarj.png',
            titulo:  `Regalos`,
            texto: `Día del niñx y fin de año
            <br>
            <br>
            Nos encanta regalar. Intentamos sorprenderl@s en estas fechas con regalos especiales, que disfruten y a las vez despierten su creatividad. Como por ejemplo, una lupa forrada con tela de peluche, una remera con luz, un cuaderno con hojas lisa y con una tapa original, un trompo con vinilos de colores para que diseñaran la mezcla imágenes que se produce al girarlo, etc. `,
          },
        },
        {
          id: 8,
          dialog: false,
          color: '#FFA004',
          posicion: {
            top: '45%',
            left: '85%'
          },
          contenido: {
            fondo: '8 Papeles Florentinos/08 fondo.png',
            imagen: '8 Papeles Florentinos/08 foto tarj.png',
            titulo:  `Papeles Florentinos`,
            texto: ` Es esa técnica renacentista donde se tiran gotas de óleos diluídas con aguarrás en un recipiente con agua. Como los colores flotan se apoya una hoja sobre el agua y se imprimen manchas únicas e irrepetibles.
            <br>
            <br>
            Cuando estas hojas se secan, cada un@ decide si las usamos para un collage, si buscamos algún dibujo escondido y lo remarcamos con marcador negro, o lo enmarcamos. `,
          },
        },
        {
          id: 9,
          dialog: false,
          color: '#5C3801',
          posicion: {
            top: '30%',
            left: '10%'
          },
          contenido: {
            fondo: '9 Maquetas/09 fondo.png',
            imagen: '9 Maquetas/09 foto tarj.png',
            titulo:  `Maquetas`,
            texto: `La posibilidad y felicidad de construir esos micromundos o espacios. 
            <br>
            <br>
            Una maqueta es una reproducción de una construcción de un lugar real o imaginario hecha en tamaño reducido.
            <br>
            <br>
            Las hay de exterior: plazas, playas, jardines, y hasta islas.
            <br>
            <br>
            Y las de interior, casas de uno o varios pisos, hoteles, cines, y hasta una casa rodante.
            <br>
            <br>
            Es un proyecto largo que combina diferentes materiales y técnicas según las necesidades.
            <br>
            <br>
            Pocas veces l@s chic@s crean los personajes que las habitan. Son los escenarios para poder jugar en casa con sus legos, petshop y demás juguetes miniatura. `,
          },
        },
        {
          id: 10,
          dialog: false,
          color: '#800080',
          posicion: {
            top: '85%',
            left: '15%'
          },
          contenido: {
            fondo: '10 Juegos y Juguetes/10 fondo.png',
            imagen: '10 Juegos y Juguetes/10 foto tarj.png',
            titulo:  `Juegos y Juguetes`,
            texto: ` Con los materiales del taller l@s chic@s crean juegos y juguetes para luego interactuar con su creación. A veces reproducen un juego tradicional, pero a su manera, como un ajedrez pero con piezas diferentes, a veces son juegos totalmente inventados por ell@s, dónde además de diseñar y construir el juego, tienen que pensar las reglas para poder jugarlo.`,
          },
        },
        {
          id: 11,
          dialog: false,
          color: '#808080',
          posicion: {
            top: '40%',
            left: '50%'
          },
          contenido: {
            fondo: '11 Talla en Piedra/11 fondo.png',
            imagen: '11 Talla en Piedra/11 foto tarj.png',
            titulo:  `Talla en Piedra`,
            texto: `Es un gran desafío, “sacar” de la piedra la forma o la figura que ella contiene. El material es Retak, una piedra que nos permite a partir de un martillo y el cincel, tallar y obtener esculturas maravillosas, que luego l@s chic@s pintan y a veces instalan en bases o cajas.
            <br>
            <br>
            En general se parte de bloques rectangulares. Con el  lápiz negro marcan el contorno de la forma que se quiere y de a poco se empieza a picar y a sacar el material sobrante hasta que nos quede la forma.  L@s chic@s se entusiasman aunque sea un proceso largo y de gran esfuerzo físico. `,
          },
        },
        {
          id: 12,
          dialog: false,
          color: '#FOAED7',
          posicion: {
            top: '60%',
            left: '15%'
          },
          contenido: {
            fondo: '12 Cajita de las Ideas/12 fondo.png',
            imagen: '12 Cajita de las Ideas/12 foto tarj.png',
            titulo:  ` Cajita de las Ideas`,
            texto: `es una caja con papelitos, en cada uno está escrito un tema o una palabra. Aquell@s chic@s que llegan al taller sin inspiración (algo que ocurre pocas veces), pueden sacar un papelito con alguna idea: “una playa”, “una familia de gatos”, “un monstruo”, etc. La mayoría de las veces, mientras van leyendo los papelitos, se escucha: ya sé! Y arrancan un proyecto que nada tiene que ver con los papelitos que sacaron.
            <br>
            <br>
            Este recurso me lo enseñó Mareína, una artista y profe de plástica de  Vicente López. `,
          },
        },
        {
          id: 13,
          dialog: false,
          color: '#8C6048',
          posicion: {
            top: '50%',
            left: '50%'
          },
          contenido: {
            fondo: '13 Arcilla/13 fondo.png',
            imagen: '13 Arcilla/13 foto tarj.png',
            titulo:  `Arcilla`,
            texto: `Es un material fundamental del taller.
            <br>
            <br>
            Su flexibilidad al manipularla permite a l@s chic@s llevar adelante sus ideas casi sin dificultad. Rápidamente incorporan el uso de las herramientas, (algunas específicas de la cerámica y otras provenientes de nuestra vida cotidiana que se adaptan perfectamente; posiblemente el pisa ajo convertido en la máquina de pelos y/o fideos, resulte de los más queridos) y también su lenguaje específico, barbotina, esmalte, coser, plancha, ahuecar, etc. lo aprenden naturalmente, mientras crean sus piezas.
            <br>
            <br>
            Recuerdo perfectamente el día que Uma de 6 años se sentó en el torno y mientras sus manos creaban una forma en el torno me dijo emocionada: “esto parece un sueño” `,
          },
        },
        {
          id: 14,
          dialog: false,
          color: '#8ADAA9',
          posicion: {
            top: '55%',
            left: '25%'
          },
          contenido: {
            fondo: '14 Collage/14 fondo.png',
            imagen: '14 Collage/14 foto tarj.png',
            titulo:  `Collage`,
            texto: `En el taller “hay de todo” y entonces los materiales nos inspiran.
            <br>
            <br>
            Muchas veces, un trabajo empieza como dibujo y termina enriquecido con otros materiales y se convierte en un collage. 
            <br>
            <br>
            Un dibujo de una playa tiene arena “de verdad”, las cortinas del dibujo de una casa son de tela, un dibujo de un jardín tiene pasto sintético…
            <br>
            <br>
            A veces una tela suave y calentita inspira a dibujar una cama y convertirla en una frazada, unas lentejuelas son convertidas en flores, y otras, los materiales se combinan entre sí, de una manera original y creativa. `,
          },
        },
        {
          id: 15,
          dialog: false,
          color: '#FF5733',
          posicion: {
            top: '63%',
            left: '70%'
          },
          contenido: {
            fondo: '15 Salidas a Museos/15 fondo.png',
            imagen: '15 Salidas a Museos/15 foto tarj.png',
            titulo:  `Visitas a Museos`,
            texto: `Buenos Aires nos ofrece un circuito de museos y galerías muy variado. Cuando aparece alguna muestra que sabemos va a enriquecer la mirada atenta de l@s chic@s organizamos una visita.
            <br>
            <br>
            Por supuesto, queremos hacer de cada exposición una experiencia única, dónde l@s chic@s sean l@s protagonistas. Cada un@, entra con su cuaderno para seguir algunas consignas y también para anotar o dibujar lo que quieran. Es su “Diario de Viaje por la muestra”. Los recorridos que por supuesto están diseñados previamente, son dinámicos y participativos. Observamos la obra a partir de preguntas y siempre nos dispara alguna actividad, a veces un juego, a veces una historia, a veces un dibujo. Lo registramos en el cuaderno. En una segunda parte, volvemos al taller. Cargados de imágenes y de información realizamos producciones vinculadas de alguna manera a la muestra.
            <br>
            <br>
            Nuestro mayor deseo es que ir a una muestra de arte quede asociada a una experiencia. `,
          },
        },
        {
          id: 16,
          dialog: false,
          color: '#EE3FC7',
          posicion: {
            top: '25%',
            left: '62%'
          },
          contenido: {
            fondo: '16 Siluetas/16 fondo.png',
            imagen: '16 Siluetas/16 foto tarj.png',
            titulo:  `Siluetas`,
            texto: ` En la terraza, l@s chic@s se recuestan sobre grandes hojas y allí les marcamos su contorno. A partir de ahí cada un@ crea su personaje, dibuja la cara, el pelo, la ropa y el calzado, algun@s agregan algún objeto. Cada un@ elije si usa tela para la ropa o la pinta con témpera o las dos cosas. Algun@s la recortan y otros crean un fondo. Otros, recortan piernas y brazos que luego unieron con ganchos mariposas y así le dieron movimiento.`,
          },
        },
        {
          id: 17,
          dialog: false,
          color: '#8B1470',
          posicion: {
            top: '90%',
            left: '70%'
          },
          contenido: {
            fondo: '17 Movibles articulados/17 fondo.png',
            imagen: '17 Movibles articulados/17 foto tarj.png',
            titulo:  `Movibles y articulados`,
            texto: ` Este proyecto implica dibujar primero y pintar después alguna figura (una persona o un animal) pero con sus miembros/partes por separado, luego los recortamos y finalmente los volvemos a unir con tuercas y tornillos para que logren movimiento. Para esto trabajamos con materiales resistentes como maderas, cartón o placas de yeso.`,
          },
        },
        {
          id: 18,
          dialog: false,
          color: '#913F02',
          posicion: {
            top: '31%',
            left: '75%'
          },
          contenido: {
            fondo: '18 Torno/18 fondo.png',
            imagen: '18 Torno/18 foto tarj.png',
            titulo:  `Torno`,
            texto: ` ¿Cómo explicar esa sensación única de hundir los dedos y abrazar la arcilla mientras va girando?
            <br>
            <br>
            ¿cómo describir esa sonrisa que empieza a dibujarse en las caras de l@s chic@s que prueban esto por primera vez? `,
          },
        },
        {
          id: 19,
          dialog: false,
          color: '#800000',
          posicion: {
            top: '80%',
            left: '29%'
          },
          contenido: {
            fondo: '19 Horno/19 fondo.png',
            imagen: '19 Horno/19 foto tarj.png',
            titulo:  `Horno de cerámica`,
            texto: `La cerámica es el resultado de todo el proceso, modelado, secado y posterior horneado, esmaltado y vuelta a hornear. Por eso requiere además del dominio de la técnica, otros  aprendizajes, como a esperar los propios tiempos del material,  del secado, y a veces también, esperar los tiempos del taller, porque la pieza no se pudo hornear. `,
          },
        },
        {
          id: 20,
          dialog: false,
          color: '#1A4E90',
          posicion: {
            top: '83%',
            left: '75%'
          },
          contenido: {
            fondo: '20 Telar/20 fondo.png',
            imagen: '20 Telar/20 foto tarj.png',
            titulo:  `Telar`,
            texto: ` Utilizamos el tejido plástico que habitualmente se usa para jardinería o construcción como base de un telar (la urdimbre), pasando telas lanas, enhebrando, etc. Creando diseños abstractos, guardas y hasta dibujos reales.`,
          },
        },
        {
          id: 21,
          dialog: false,
          color: '#608394',
          posicion: {
            top: '90%',
            left: '90%'
          },
          contenido: {
            fondo: '21 Telas/21 fondo.png',
            imagen: '21 Telas/21 foto tarj.png',
            titulo:  `Telas`,
            texto: ` Materiales que inspiran
            <br>
            <br>
            Telas lisas, estampadas, de todos los colores, finitas, gruesas.
            <br>
            <br>
            Son cortinas para una casa, telones de escenarios, sábanas, frazadas y por supuesto ropa para un personaje. Pero también, pieles de animales y bellos trabajos abstractos. `,
          },
        },
        {
          id: 22,
          dialog: false,
          color: '#808000',
          posicion: {
            top: '60%',
            left: '55%'
          },
          contenido: {
            fondo: '22 Libro de artistas/22 fondo.png',
            imagen: '22 Libro de artistas/22 foto tarj.png',
            titulo:  `Libros de Artistas`,
            texto: ` Un sábado por la tarde, paso con el auto por la esquina de la plaza de Echeverría y Mariano Acha, en Buenos Aires, y veo una pila enorme de libros antiguos de contabilidad. Me detengo y los empiezo a revisar y enseguida me vienen las caras de felicidad que seguramente veamos la semana siguiente en el taller, cuando les contemos que él/la que quiera va a poder crear un Libro de Artista usando como soporte estos “tesoros”, unos libros que sácandole las primeras páginas escritas por un prolijo contador, les quedaban a cada uno cientos (sí! Cientos) de hojas para crear, lo que quisieran. Y así ocurrió. Rápidamente, cada libro se convirtió en historias dibujadas, libros de texturas y collage, libros de gatos, etc. 
            <br>
            <br>
            (No tod@s pudieron terminarlos, pero de todas maneras seguramente, fue gran experiencia para tod@s ell@s.) `,
          },
        },
        {
          id: 23,
          dialog: false,
          color: '#F4D03F',
          posicion: {
            top: '90%',
            left: '10%'
          },
          contenido: {
            fondo: '23 Azulejos/23 fondo.png',
            imagen: '23 Azulejos/23 foto tarj.png',
            titulo:  `Azulejos`,
            texto: `Materiales que inspiran
            <br>
            <br>
            A veces son el soporte (base) de un dibujo con marcadores indelebles y/o collage. A veces los usamos en maquetas y otras con pequeños pedazos para realizar un trencadis. (dibujo con azulejos) `,
          },
        },
        {
          id: 24,
          dialog: false,
          color: '#8B6CA1',
          posicion: {
            top: '80%',
            left: '20%'
          },
          contenido: {
            fondo: '24 Biblioteca/24 fondo.png',
            imagen: '24 Biblioteca/24 foto tarj.png',
            titulo:  `Biblioteca`,
            texto: `En el taller hay una biblioteca a la que recurrimos para inspirarnos, conocer artistas y sus obras, cómo usan los diferentes materiales que nosotros también usamos en el taller. y de a poco ir construyendo una mirada sensible y crítica porque creemos que esto es lo que los hace más autónomos en la producción de ideas y de imágenes. 
            <br>
            <br>
            Pero no sólo hay libros de arte, allí podemos encontrar enciclopedias de animales, libros de jardinería, autos, el sistema solar y diversos temas que interesan a los chicos y que ayudan a enriquecer sus imágenes. `,
          },
        },
        {
          id: 25,
          dialog: false,
          color: '#A9CCE3',
          posicion: {
            top: '70%',
            left: '30%'
          },
          contenido: {
            fondo: '25 Materiales/25 fondo.png',
            imagen: '25 Materiales/25 foto tarj.png',
            titulo:  `Materiales`,
            texto: ` Pinceles Gruesos, medianos y finitos, chatos y redondos. Para usar con témperas, acuarelas o esmaltar cerámica.
            <br>
            <br>
            Témperas, marcadores, lápices negros de colores, óleo pastel, tijeras, pegamento, gomas de borrar y sacapuntas. `,
          },
        },
        {
          id: 26,
          dialog: false,
          color: '#FF0000',
          posicion: {
            top: '60%',
            left: '40%'
          },
          contenido: {
            fondo: '26 Trabajos con Maderas/26 fondo.png',
            imagen: '26 Trabajos con Maderas/26 foto tarj.png',
            titulo:  `Trabajos con maderas`,
            texto: `Recortes de madera se transforman en naves, robots, pequeños muebles de una maqueta o simplemente como soporte (base) para dibujar, pintar, o crear una escultura abstracta. `,
          },
        },
        {
          id: 27,
          dialog: false,
          color: '#5A7A5D',
          posicion: {
            top: '40%',
            left: '60%'
          },
          contenido: {
            fondo: '27 Pinturas Circulares/27 fondo.png',
            imagen: '27 Pinturas Circulares/27 foto tarj.png',
            titulo:  `Pinturas Circulares`,
            texto: `Para este trabajo se necesitan 2 personas, una torneta, hojas, cinta y témperas,(opcional un palito para mezclar o dibujar). Primero pegamos la hoja con cinta en la torneta, luego mientras un@ gira la torneta, otr@ tira diferentes colores de temperas sobre la hoja, si quiere puede utilizar un palito para usar sobre la hoja mientras la torneta gira. Cuando terminan, intercambian la tarea. `,
          },
        },
        {
          id: 28,
          dialog: false,
          color: '#000080',
          posicion: {
            top: '30%',
            left: '70%'
          },
          contenido: {
            fondo: '28 Zoom/28 fondo.png',
            imagen: '28 Zoom/28 foto tarj.png',
            titulo:  `Zoom`,
            texto: `El 2 de marzo de 2020 comenzó el ciclo lectivo en el taller. 15 días después por el Covid 19 se decretó el aislamiento social obligatorio. Esto significó, entre tantas otras cosas, que ya no podíamos encontrarnos en el taller.  Entonces, empezamos a conectarnos para realizar diferentes propuestas (según las edades) en cada encuentro. Todo un desafío para ell@s y para mí. Sin embargo logramos crear un espacio virtual de encuentro donde además de hacer lo que nos gusta, compartimos historias, y charlamos.`,
          },
        },
        {
          id: 29,
          dialog: false,
          color: '#FFAO7A',
          posicion: {
            top: '20%',
            left: '80%'
          },
          contenido: {
            fondo: '29 Técnicas y propuestas/29 fondo.png',
            imagen: '29 Técnicas y propuestas/29 foto tarj.png',
            titulo:  `Materiales y propuestas`,
            texto: ` A veces un material nos despierta una idea, a veces una idea nos conduce al material.
            <br>
            <br>
            Trabajamos con los materiales convencionales de la plástica y con otros.
            <br>
            <br>
            De a poco los chicos empiezan a ver en los objetos y materiales un disparador para un trabajo suyo o de algunos de sus compañeros. 
            <br>
            <br>
            Y “contagian” a su familia que nos proveen de muchos materiales que son muy aprovechados por l@s chic@s, desde azulejos que sobraron de una remodelación, recortes de telas de una mamá diseñadora (o ruedas de bicicletas), etc.
            <br>
            <br>
            A veces, la idea nos conduce a la búsqueda del material adecuado para expresarnos. Por eso intentamos que haya “de todo” en el taller. Es a partir de la experiencia que los chicos prueban y descubren las posibilidades que se esconden detrás de materiales y herramientas.
            <br>
            <br>
            Las técnicas y materiales se usan en función de lo que se quiere expresar.
            <br>
            <br>
            No es la técnica lo que expresa sino las emociones y los sentimientos.
            <br>
            <br>
            Quien utiliza los materiales le da forma y significado.
            <br>
            <br>
            En manos de los chicos, TODO puede transformarse en material para producir, inventar, construir. `,
          },
        },
        {
          id: 30,
          dialog: false,
          color: '#FOAED7',
          posicion: {
            top: '10%',
            left: '90%'
          },
          contenido: {
            fondo: '30 Mueble de cajoncitos/30 fondo.png',
            imagen: '30 Mueble de cajoncitos/30 foto tarj.png',
            titulo:  `Muebles de Cajoncitos`,
            texto: ` Es un mueble al alcance de los chicx@ con diferentes materiales, que pueden utilizar a medida que vayan necesitando. La idea es que vayan adquiriendo mayor autonomía.`,
          },
        },
      ]
    }
  },
  mounted() {
    this.posicionarBotones()
    window.addEventListener("resize", this.posicionarBotones);
  },
  created() {
  },
  methods: {
    posicionarBotones() {
      // let boton = document.getElementsByClassName('boton')

      // boton.style.left = '60%'
      // boton.style.top =  '0%'
      // boton.style.display = 'block'
    }
  }
}
</script>

<style>
.botonModal {
  position: absolute !important;
}

.flex-row {
  display: flex;
}

.flex-center {
  display: flex;
  justify-content: center;
}

.ov-none {
  overflow: hidden;
}

.imagenFondo {
  position: absolute;
}

.boton {
  position: absolute;
}

.contenedorEstrellas {
  position: relative;
}

.floating { 
  animation-name: floating;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in-out;
}
 
@keyframes floating {
  0% { transform: translate(0,  0px); }
  50%  { transform: translate(0px, 3px); }
  100%   { transform: translate(-0, -0px); }   
}

</style>


