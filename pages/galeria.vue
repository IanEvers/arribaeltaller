<template>
    <v-col
        cols="16"
        sm="12"
        class="margin"
    >
        <v-sheet
            rounded="lg"
        >
            <h2 class="rojo"> Galería </h2>
            <v-carousel>
                <v-carousel-item
                v-for="(item,i) in items"
                :key="i"
                :src="item.src"
                reverse-transition="fade-transition"
                transition="fade-transition"
                ></v-carousel-item>
            </v-carousel>
        </v-sheet>
    </v-col>
</template>

<script>
export default {
    data () {
        return {
            items: [
                {
                    src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                },
                {
                    src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
                },
                {
                    src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
                },
                {
                    src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                },
            ],
        }
    }
}
</script>

<style >

.margin {
    margin: 2rem;
}

.rojo {
    color: #ff5733;
    padding: 1rem;
}

.v-responsive__content {
    width: 90vw !important;
}
</style>