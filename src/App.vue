<template>
  <div id="app" v-if="step!='camera'">
    <Enter v-if="step=='enter'" @change="change"/>
    <Start v-if="step=='start'" @change="change"/>
    <Video v-if="step=='video'" @change="change"/>
    <Sale v-if="step=='sale'" @change="change"/>
    <Bonus v-if="step=='bonus'" @change="change"/>
    <Item v-if="step=='item'" @change="change"/>
  </div>
</template>

<script>
import Enter from './components/Enter.vue'
import Start from './components/Start.vue'
import Video from './components/Video.vue'
import Bonus from './components/Bonus.vue'
import Sale from './components/Sale.vue'
import Item from './components/Item.vue'
import jsQR from 'jsqr';

const video = document.createElement('video');
var canvasElement = document.createElement("canvas");
var canvas = canvasElement.getContext("2d");

export default {
  name: 'App',
  components: {
    Enter,
    Start,
    Sale,
    Video,
    Bonus,
    Item
  },
  data() {
    return {
      qrValue: null,
      step: 'video',
      // step: 'item',
    }
  },
  mounted() {
    // this.change('enter');
    // navigator.mediaDevices.getUserMedia({ video: { facingMode: "environment" } }).then((stream) => {
    //   video.srcObject = stream;
    //   console.log("stream", stream)
    //   video.setAttribute("playsinline", true); // required to tell iOS safari we don't want fullscreen
    //   video.play();
    //   requestAnimationFrame(this.tick);
    // });

    // document.getElementById('aks-marker').addEventListener('markerFound', () => {
      document.addEventListener('click', () => {
        if(this.step !== 'camera') return;
        this.step = 'bonus';
      })
    // })
  
  },
  methods: {
    tick() {
      if (video.readyState === video.HAVE_ENOUGH_DATA) {
          canvasElement.height = video.videoHeight;
          canvasElement.width = video.videoWidth;
          canvas.drawImage(video, 0, 0, canvasElement.width, canvasElement.height);
          const imageData = canvas.getImageData(0, 0, canvasElement.width, canvasElement.height);
          const code = jsQR(imageData.data, imageData.width, imageData.height, {
            inversionAttempts: "dontInvert",
          });
          if(code) {
            console.log(code.data);
          }
        }
      
      requestAnimationFrame(this.tick);
    },

    change(event) {
      if(event == 'camera') document.getElementById('scene').style.display = "block";
      else document.getElementById('scene').style.display = "none";
      setTimeout(() => {
        this.step = event;
      }, 100)
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

* {
    font-family: Roboto;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    /* color: #23213C; */
}

#app {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: white;
  padding: 40px;
  overflow-x: auto;
  /* max-width: 500px; */
}

h3 {
  font-style: normal;
  font-weight: 600;
  font-size: 36px;
  line-height: 36px;
  padding-bottom: 20px;
}

.button-row {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
}
.button-row > *:not(:last-child) {
  margin-right: 20px;
}
.button-column {
  margin-top: 20px;
  display: flex;
  width: 50%;
  flex-direction: column;
  justify-content: space-between;
}
.button-column > *:not(:last-child) {
  margin-bottom: 20px;
}
</style>
