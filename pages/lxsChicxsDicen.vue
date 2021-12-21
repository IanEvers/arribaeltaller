<template>
     <v-col
        cols="16"
        sm="12"
    >
        <v-sheet>
            <h2 class="lila">Lxs Chicxs dicen</h2>
            <v-card 
                class="miniMargen"
                v-for="chico in chicos"
                :key="chico.titulo"
            >
               <div class="d-md-flex">
                   <div class="min-width">
                        <h2 class="chicos"> {{ chico.titulo }}</h2>
                        <p v-html="chico.descripcion"> </p>
                   </div>
                    <v-img
                        class="fotoChicos"
                        :src="chico.imagen"
                    ></v-img>
               </div>
            </v-card>
        </v-sheet>
    </v-col>
</template>
<script>
export default {
    data () {
        return {
            chicos: [
                {
                    titulo: 'Este es un taller de Artes Marciales?',
                    descripcion: `Preguntó Joaquín de 6 años su primer día, antes de entrar al taller. Con miedo a decepcionarlo, respondo que no. Es un taller de artes plásticas, digo, para dibujar, pintar, construir… 
                                <br>
                                <br>
                                Uf, responde Joaquín aliviado, menos mal!
                                <br>
                                <br>
                                Todo comienza con las ganas. 
                                <br>
                                <br>
                                Ganas de usar materiales y herramientas que permitan expresar ideas y sentimientos personales a través del lenguaje plástico.`,
                    imagen: '1.jpeg'
                },
                {
                    titulo: '“Esto parece un sueño”',
                    descripcion: `Dice Uma mientras sus manos abrazan la arcilla en el torno (Uma, 6 años).
                    <br>
                    <br>
                    El arte nos permite crear mundos posibles y el taller es el espacio ideal para empezar a diseñarlos.`,
                    imagen: '2.jpeg'
                },
                {
                    titulo: '“No puedo dibujar lo que no me gusta”',
                    descripcion: `dice Francisco, de 7 años. Francisco quiere hacerle una tarjeta de cumpleaños a su mejor amigo, como no se le ocurre qué dibujar, le pregunto qué cosas le gustan a su amigo. El fútbol, me contesta. Bueno, podés dibujar algo de fútbol. A lo que Francisco responde: - a mí el fútbol no me gusta. No puedo dibujar lo que no me gusta.
                    <br>
                    <br>
                    En el taller, lxs chicxs expresan sus propias ideas. Dibujamos, pintamos, construimos aquello que nos despierte un sentimiento, una emoción. Con este rol activo en su propio aprendizaje logran experiencias más profundas y conocimientos que duran para siempre.`,
                    imagen: '3.jpeg'
                },
                {
                    titulo: 'Ahora te lo dibujo',
                    descripcion: `Viole fue a la casa de su abuela a dormir. Al día siguiente cuando su papá la fue a buscar, le preguntó qué habían hecho. Viole fue a buscar papel y lápiz y le respondió, ahora te lo dibujo.
                    <br>
                    <br>
                    Viole tiene 4 años.
                    <br>
                    <br>
                    Con la expresión plástica se “dicen” cosas que no se podrían decir de otra manera.`,
                    imagen: '4.jpeg'
                },
                {
                    titulo: 'La experiencia de Emi y su nave',
                    descripcion: `Emi llegó al taller con una idea: construir una nave que ella pudiera entrar y usar, sabía perfectamente cómo sería.
                    <br>
                    <br>
                    Pegó dos cajas, las abrió, le puso una palanca, botones, un volante y varios detalles. La pintó por dentro y por fuera, le hizo la puerta y hasta le puso candado! Sólo ella podría entrar.
                    <br>
                    <br>
                    Varios meses trabajó en este proyecto, lo terminó y se llevó la nave a su casa. Su mamá me cuenta cómo Emi juega en su casa con su nave.
                    <br>
                    <br>
                    Pasaron 2 años y Emi me cuenta con un dejo de tristeza que el otro día jugó con su nave (a la que le costó entrar) pero que la tuvieron que ayudar para salir porque la nave ya le quedaba chica. 
                    <br>
                    <br>
                    Otra más de Emi:
                    <br>
                    <br>
                    Emi entra al taller, abre sus manos y me muestra 4 ruedas de madera, “quiero hacer un monopatín que yo pueda andar” dice. Manos a la obra! 
                    <br>
                    <br>
                    La mayoría de lxs chicxs ya poseen las habilidades que necesitan para realizar su trabajo, nuestro objetivo es facilitar experiencias.`,
                    imagen: '5.jpeg'
                },
                {
                    titulo: '“Me quedó un arco iris, ahora puedo ver el arco iris cada vez que quiera”',
                    descripcion: `-Felicitas, 6 años. Es importante para nosotrxs que lxs chicxs que lxs chicxs puedan conectar entre la obra y su propia vida`,
                    imagen: '6.jpeg'
                },
                {
                    titulo: '“Mamá, prometeme que siempre me vas a dejar venir a la Noche del Taller!”',
                    descripcion: `Pedido de Sofi a su mamá cuando la vino a buscar, a la mañana siguiente de la Noche del Taller.`,
                    imagen: '7.jpeg'
                },
            ]
        }
    },
}
</script>

<style scoped>

.chicos {
    padding: 1rem;
    font-size: 1.5rem;
}

.miniMargen {
    margin: 1rem;
}

.flex {
    display: flex;
    justify-content: space-between;
}

@media (min-width: 1900px) {
    .min-width {
        min-width: 51vw;
    }
}

@media (min-width: 960px) {
    .fotoChicos {
        max-width: 40vw;
    }
}

.lila {
    color: #8B6CA1;
}

.losChicos {
    margin-top: 2rem;
}
</style>