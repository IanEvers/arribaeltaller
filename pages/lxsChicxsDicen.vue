<template>
     <v-col
        cols="16"
        sm="12"
    >
        <v-sheet
            rounded="lg"
        >
            <h2 class=" lila">Los Chicxs dicen</h2>
            <v-card 
                v-for="chico in chicos"
                :key="chico.titulo"
            >
               <h2 class="chicos"> {{ chico.titulo }}</h2>
               <p> {{ chico.descripcion }}</p>
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
                    descripcion: `Preguntó Joaquín de 6 años su primer día, antes de entrar al taller. Con miedo a decepcionarlo, respondo que no. Es un taller de artes plásticas, digo, para dibujar, pintar, construir… Uf, responde Joaquín aliviado, menos mal! Todo comienza con las ganas. Ganas de usar materiales y herramientas que permitan expresar ideas y sentimientos personales a través del lenguaje plástico.`
                },
                {
                    titulo: '“Esto parece un sueño”',
                    descripcion: `Dice Uma mientras sus manos abrazan la arcilla en el torno (Uma, 6 años). El arte nos permite crear mundos posibles y el taller es el espacio ideal para empezar a diseñarlos.`
                },
                {
                    titulo: '“No puedo dibujar lo que no me gusta”',
                    descripcion: `dice Francisco, de 7 años. Francisco quiere hacerle una tarjeta de cumpleaños a su mejor amigo, como no se le ocurre qué dibujar, le pregunto qué cosas le gustan a su amigo. El fútbol, me contesta. Bueno, podés dibujar algo de fútbol. A lo que Francisco responde: - a mí el fútbol no me gusta. No puedo dibujar lo que no me gusta. En el taller, l@s chic@s expresan sus propias ideas. Dibujamos, pintamos, construimos aquello que nos despierte un sentimiento, una emoción. Con este rol activo en su propio aprendizaje logran experiencias más profundas y conocimientos que duran para siempre.`
                },
                {
                    titulo: 'Ahora te lo dibujo',
                    descripcion: `Viole fue a la casa de su abuela a dormir Al día siguiente cuando su papá la fue a buscar, le preguntó qué habían hecho. Viole fue a buscar papel y lápiz y le respondió, ahora te lo dibujo. Viole tiene 4 años. Con la expresión plástica se “dicen” cosas que no se podrían decir de otra manera.`
                },
                {
                    titulo: 'La experiencia de Emi y su nave',
                    descripcion: `Emi llegó al taller con una idea: construir una nave que ella pudiera entrar y usar, sabía perfectamente cómo sería. Pegó dos cajas, las abrió, le puso una palanca, botones, un volante y varios detalles. La pintó por dentro y por fuera, le hizo la puerta y hasta le puso candado! Sólo ella podría entrar. Varios meses trabajó en este proyecto, lo terminó y se llevó la nave a su casa. Su mamá me cuenta cómo Emi juega en su casa con su nave. Pasaron 2 años y Emi me cuenta con un dejo de tristeza que el otro día jugó con su nave (a la que le costó entrar) pero que la tuvieron que ayudar para salir porque la nave ya le quedaba chica. Otra más de Emi Emi entra al taller, abre sus manos y me muestra 4 ruedas de madera, “quiero hacer un monopatín que yo pueda andar” dice. Manos a la obra! La mayoría de l@s chic@s ya poseen las habilidades que necesitan para realizar su trabajo, nuestro objetivo es facilitar experiencias.`
                },
                {
                    titulo: '“Me quedó un arco iris, ahora puedo ver el arco iris cada vez que quiera”',
                    descripcion: `-Felicitas, 6 años. Es importante para nosotr@s que l@s chic@s que l@s chic@s puedan conectar entre la obra y su propia vida`
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

.lila {
    color: #8B6CA1;
}

.losChicos {
    margin-top: 2rem;
}
</style>