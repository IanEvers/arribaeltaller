<template>

  <v-col
    cols="16"
    sm="12"
  >

    <div class="confetti" v-if="idea == 'sacada'">
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
      <div class="confetti-piece"></div>
    </div>

    <v-sheet class="flex-column-center">
      <h2 class="caja text-center pa-2">Caja de las ideas</h2>

      <div class="cajaIdeasContenedor">


        <div class="cube" ref="cubo" @click="sacarIdea()" :class="{ ideaSacada: idea == 'sacando' }" v-if="idea != 'sacada'">
          <div class="side front">
            <img src="cajaIdeas/texturaCaja.png" alt="">
          </div>
          <div class="side back"> <img src="cajaIdeas/texturaCaja.png" alt=""></div>
          <div class="side left"> <img src="cajaIdeas/texturaCaja.png" alt=""></div>
          <div class="side right"> <img src="cajaIdeas/texturaCaja.png" alt=""></div>
          <div class="side top"> <img src="cajaIdeas/texturaCaja.png" alt=""></div>
          <div class="side bottom"> <img src="cajaIdeas/texturaCaja.png" alt=""></div>
        </div>

        <div v-else>
          <h2 class="ideaTexto">idea: idea numero {{Math.floor(Math.random() * 1000)}}</h2>

        </div>
      </div>

      <!-- <div class="cajaIdeas">
        <img src="cajaIdeas/texturaCaja.png" alt="" style="background-image: url(/cajaIdeas/texturaCaja.png);">
      </div> -->

    </v-sheet>
  </v-col>

</template>

<script>

export default {
  data () {
    return {
      idea: 'no sacada',
      ideas: [
        'idea 1'
      ]
    }
  },
   
  methods: {
   
    sacarIdea() {
      this.idea = 'sacando'

      addEventListener("webkitAnimationEnd", this.myEndFunction);
    },

    myEndFunction( ) {
      console.log('end')
      this.idea = 'sacada'

    }

  }

}

</script>

<style>

.caja {
  color: #002a03;
}

.flex-column-center {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  min-height: 80vh;
}

.cajaIdeas {
  max-width: 90vw;
}

.cajaIdeasContenedor {
  width: 400px;
  height: 400px;
  flex: 1;
  border-radius: 4px;
  display: flex;
  justify-content: center;
  align-items: center;
  perspective: 800px;
  perspective-origin: top right;
  z-index: 1;
}

/* The child element, with 3D tranforms preserved */
.cube {
  position: relative;
  width: 200px;
  height: 200px;
  transform-style: preserve-3d;
  animation: cubeRotate 10s linear infinite;
  
}



img {
  width: 200px;
  height: 200px;
}

/* The sides of the cube, absolutely positioned */
.side {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 1;
  border: 2px solid rgba(0, 0, 0, 0);
}

/* Background colors for the cube's sides to help visualize the work */
.front {
  background-color: #d50000; 
  transform: translateZ(100px);
}

.back {
  background-color: #aa00ff;
  transform: translateZ(-100px);
}

.left { 
  background-color: #304ffe; 
  transform: rotateY(90deg) translateZ(100px);
}
.right {
  background-color: #0091ea; 
  transform: rotateY(-90deg) translateZ(100px);
}

.top {
  background-color: #00bfa5; 
  transform: rotateX(90deg) translateZ(100px);
}

.bottom {
  background-color: #64dd17; 
  transform: rotateX(-90deg) translateZ(100px);
}

@keyframes cubeRotate {
  from { transform: rotateY(0deg) rotateX(720deg) rotateZ(0deg); }
  to { transform: rotateY(360deg) rotateX(0deg) rotateZ(360deg); }
}

.ideaSacada {
  animation: cubeEnd 5s linear;
}

.ideaTexto {
  animation: textoIdea 1s linear;
}

@keyframes cubeEnd {
  0% {
    -webkit-transform: scale(1)  rotateY(0deg) rotateX(720deg) rotateZ(0deg);;
            transform: scale(1)  rotateY(0deg) rotateX(720deg) rotateZ(0deg);;
  }
  100% {
    -webkit-transform: scale(5) rotateY(360deg) rotateX(0deg) rotateZ(360deg);;
            transform: scale(5) rotateY(360deg) rotateX(0deg) rotateZ(360deg);;
  }
}

@keyframes textoIdea {
  0% {
    -webkit-transform: rotateY(0deg) rotateX(720deg) rotateZ(0deg);;
            transform: rotateY(0deg) rotateX(720deg) rotateZ(0deg);;
  }
  100% {
    -webkit-transform: rotateY(360deg) rotateX(0deg) rotateZ(360deg);;
            transform: rotateY(360deg) rotateX(0deg) rotateZ(360deg);;
  }
}

.confetti {
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    width: 100%;
    height: 100%;
    overflow: hidden;
    z-index: 1000;
}
.confetti-piece {
    position: absolute;
    width: 10px;
    height: 30px;
    background: #ffd300;
    top: 0;
    opacity: 0;
}
.confetti-piece:nth-child(1) {
    left: 7%;
    -webkit-transform: rotate(-40deg);
    transform: rotate(-40deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 182ms;
    animation-delay: 182ms;
    -webkit-animation-duration: 1116ms;
    animation-duration: 1116ms;
}
.confetti-piece:nth-child(2) {
    left: 14%;
    -webkit-transform: rotate(4deg);
    transform: rotate(4deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 161ms;
    animation-delay: 161ms;
    -webkit-animation-duration: 1076ms;
    animation-duration: 1076ms;
}
.confetti-piece:nth-child(3) {
    left: 21%;
    -webkit-transform: rotate(-51deg);
    transform: rotate(-51deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 481ms;
    animation-delay: 481ms;
    -webkit-animation-duration: 1103ms;
    animation-duration: 1103ms;
}
.confetti-piece:nth-child(4) {
    left: 28%;
    -webkit-transform: rotate(61deg);
    transform: rotate(61deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 334ms;
    animation-delay: 334ms;
    -webkit-animation-duration: 708ms;
    animation-duration: 708ms;
}
.confetti-piece:nth-child(5) {
    left: 35%;
    -webkit-transform: rotate(-52deg);
    transform: rotate(-52deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 302ms;
    animation-delay: 302ms;
    -webkit-animation-duration: 776ms;
    animation-duration: 776ms;
}
.confetti-piece:nth-child(6) {
    left: 42%;
    -webkit-transform: rotate(38deg);
    transform: rotate(38deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 180ms;
    animation-delay: 180ms;
    -webkit-animation-duration: 1168ms;
    animation-duration: 1168ms;
}
.confetti-piece:nth-child(7) {
    left: 49%;
    -webkit-transform: rotate(11deg);
    transform: rotate(11deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 395ms;
    animation-delay: 395ms;
    -webkit-animation-duration: 1200ms;
    animation-duration: 1200ms;
}
.confetti-piece:nth-child(8) {
    left: 56%;
    -webkit-transform: rotate(49deg);
    transform: rotate(49deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 14ms;
    animation-delay: 14ms;
    -webkit-animation-duration: 887ms;
    animation-duration: 887ms;
}
.confetti-piece:nth-child(9) {
    left: 63%;
    -webkit-transform: rotate(-72deg);
    transform: rotate(-72deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 149ms;
    animation-delay: 149ms;
    -webkit-animation-duration: 805ms;
    animation-duration: 805ms;
}
.confetti-piece:nth-child(10) {
    left: 70%;
    -webkit-transform: rotate(10deg);
    transform: rotate(10deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 351ms;
    animation-delay: 351ms;
    -webkit-animation-duration: 1059ms;
    animation-duration: 1059ms;
}
.confetti-piece:nth-child(11) {
    left: 77%;
    -webkit-transform: rotate(4deg);
    transform: rotate(4deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 307ms;
    animation-delay: 307ms;
    -webkit-animation-duration: 1132ms;
    animation-duration: 1132ms;
}
.confetti-piece:nth-child(12) {
    left: 84%;
    -webkit-transform: rotate(42deg);
    transform: rotate(42deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 464ms;
    animation-delay: 464ms;
    -webkit-animation-duration: 776ms;
    animation-duration: 776ms;
}
.confetti-piece:nth-child(13) {
    left: 91%;
    -webkit-transform: rotate(-72deg);
    transform: rotate(-72deg);
    -webkit-animation: makeItRain 1000ms infinite ease-out;
    animation: makeItRain 1000ms infinite ease-out;
    -webkit-animation-delay: 429ms;
    animation-delay: 429ms;
    -webkit-animation-duration: 818ms;
    animation-duration: 818ms;
}
.confetti-piece:nth-child(odd) {
    background: #7431e8;
}
.confetti-piece:nth-child(even) {
    z-index: 1;
}
.confetti-piece:nth-child(4n) {
    width: 5px;
    height: 12px;
    -webkit-animation-duration: 2000ms;
    animation-duration: 2000ms;
}
.confetti-piece:nth-child(3n) {
    width: 3px;
    height: 10px;
    -webkit-animation-duration: 2500ms;
    animation-duration: 2500ms;
    -webkit-animation-delay: 1000ms;
    animation-delay: 1000ms;
}
.confetti-piece:nth-child(4n-7) {
  background: red;
}
@-webkit-keyframes makeItRain {
    from {opacity: 0;}
    50% {opacity: 1;}
    to {-webkit-transform: translateY(350px);}
}

@keyframes makeItRain {
    from {opacity: 0;}
    50% {opacity: 1;}
    to {-webkit-transform: translateY(350px);}
}


</style>