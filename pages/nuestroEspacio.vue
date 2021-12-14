<template>
    <v-col
        cols="16"
        sm="12"
    >
        <v-sheet
            rounded="lg"
        >
                <h2 class="violeta">Nuestro Espacio</h2>

                <v-img
                    class="d-md-none nuestroEspacioImagen"
                    contain
                    src="imagen nuestro esp.jpg"
                    width="75vw"
                > </v-img>
            <div class="nuestroEspacio">
                <p>Nuestro espacio, nuestro temenos.
                    -En la antigua Grecia se llamaba Temenos al espacio sagrado, un círculo mágico, delimitado y con reglas especiales dónde "suceden libremente acontecimientos extraordinarios" (del libro Free play, de S. Nachmanotovich) Leo esta definicíón e inmediatamente llegan a mi cabeza las imágenes de nuestro taller y de las cosas que allí ocurren. Nuestro espacio tiene grandes ventanales que miran la hermosa terraza por dónde entra la luz del día desde que sale hasta que se pone el sol. escenario de nuestros proyectos creativos más diversos en un clima de disfrute y alegría. En el centro del salón se despliegan las mesas y las banquetas, dónde generalmente cada un@ ya tiene su "lugar" para sentarse y trabajar. Las paredes están cubiertas por: estantes, los más altos con los trabajos de cada grupo y los más bajos con materiales para que estén a la vista y al alcance; un mueble de madera con cajoncitos con materiales y herramientas, una estantería metálica, dónde entre esmaltes, yeso y cartones, se asoma la biblioteca. También en las paredes hay colgados cuadros con fotos de l@s chic@s que asistieron al taller desde que comenzamos hacer las muestras de fin de año en 2005.
                    A la altura del piso, distintos canastos con telas, cajas de cartón con cartones y materiales de deshecho, el cajón de las maderas, el torno de alfarería y seguramente algunas sorpresas más. Muchas veces, vemos a l@s chic@s caminando por el espacio mirando detenidamente todo "buscando" inspiración, y la encuentran!Cuando el clima nos acompaña, extendemos el taller hasta la terraza y no podemos dejar de nombrar la noche del taller, y cómo este espacio se transforma para esta experiencia nocturna. Como decimos siempre, "Arriba el Taller es un espacio de encuentro entre l@s chic@s y el arte".</p>
                <v-img
                    class="d-none d-md-block fotoNuestroEspacio"
                    contain
                    src="imagen nuestro esp.jpg"
                    width="512"
                ></v-img>
            </div>
        </v-sheet>
    </v-col>
</template>
<script>
export default {
    
}
</script>

<style scoped>
.nuestroEspacio {
    display: flex;
}

.violeta {
    color: #8B1470;
}

.nuestroEspacioImagen {
    
    margin:  1rem auto;
}


</style>