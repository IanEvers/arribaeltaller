<template>
    <v-col
        cols="16"
        sm="12"
        class="margin"
    >
        <v-sheet>
            <h2 class="rojo"> Galería </h2>
            <v-carousel
                height="70vh"
                hide-delimiters
            >
                <v-carousel-item
                    v-for="(item,i) in items"
                    :key="i"
                    :src="item"
                    reverse-transition="scroll-y-transition"
                    transition="slide-x-transition"
                    contain
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
                '/GALERIA OK/2011 aet 015.jpeg',
                '/GALERIA OK/20170412_154356.jpeg',
                '/GALERIA OK/20170504_181358.jpeg',
                '/GALERIA OK/20181102_165440.jpeg',
                '/GALERIA OK/20181107_162300.jpeg',
                '/GALERIA OK/20181215_143851.jpeg',
                '/GALERIA OK/20190105_213113.jpeg',
                '/GALERIA OK/20190105_230838.jpeg',
                '/GALERIA OK/20211025_111513.jpeg',
                '/GALERIA OK/20211119105133382-1.jpg',
                '/GALERIA OK/20211119105133382-4.jpg',
                '/GALERIA OK/collage.jpeg',
                '/GALERIA OK/Copia (2) de multiespacio 119.jpeg',
                '/GALERIA OK/Copia de a 039.jpeg',
                '/GALERIA OK/DSC_0352.jpeg',
                '/GALERIA OK/DSC00596.jpeg',
                '/GALERIA OK/DSC00661.jpeg',
                '/GALERIA OK/DSC01436.jpeg',
                '/GALERIA OK/DSC01780.JPG',
                '/GALERIA OK/DSC07013.jpeg',
                '/GALERIA OK/DSC07083.jpeg',
                '/GALERIA OK/DSC07536.jpeg',
                '/GALERIA OK/DSC08914.jpeg',
                '/GALERIA OK/image.png',
                '/GALERIA OK/IMG_20190228_133230_354.jpg',
                '/GALERIA OK/IMG_20200118_143154_999.jpeg',
                '/GALERIA OK/IMG-20200215-WA0023.jpeg',
                '/GALERIA OK/juli 098.jpeg',
                '/GALERIA OK/macba.jpeg',
                '/GALERIA OK/muestra 4.jpeg',
                '/GALERIA OK/noche del taller 026.jpeg',
                '/GALERIA OK/plastilina.jpeg',
                '/GALERIA OK/retrato.jpeg',
                '/GALERIA OK/WhatsApp Image 2021-12-06 at 11.20.06 PM.jpeg',
                '/GALERIA OK/Copia de trabajos 016.jpg',
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