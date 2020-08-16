<template>
  <div class="container-fluid nopadding">
    <v-vanta effect="net" :options="options" class="vanta"></v-vanta>
    <div class="card profileInfo">
      <h1>Hi, I'm <b style="color:lightpink">Mary grace Cordoto</b>. </h1>
      <h1>I am a Web Developer.</h1>
      <center><button id="viewWork" class="test" type="button" @click="redirect('/about')">More</button></center>
    </div>
  </div>
</template>
<script>
import VVanta from 'vue-vanta'
import router from '../router'
export default {
  components: { VVanta },
  data () {
    return {
      options: {
        mouseControls: true,
        touchControls: true,
        gyroControls: false,
        minHeight: 200.00,
        minWidth: 200.00,
        scale: 1.00,
        scaleMobile: 1.00,
        color: 0xa07785,
        backgroundColor: 0x0,
        points: 12.00,
        maxDistance: 17.00,
        spacing: 18.00
      }
    }
  },
  methods: {
    redirect (url) {
      router.push(url)
    }
  }
}
</script>
<style>
.nopadding{
  padding: 0px;
}
.vanta-container{
  height: 100vh !important;
}
.section-background{
  height: 100vh;
}
.profileInfo {
  font-style: initial;
  color: white;
  background: transparent !important;
  position: absolute !important;
  top: 50% !important;
  left: 50% !important;
  margin-right: -50% !important;
  transform: translate(-50%, -50%) !important;
}

.test {
  background-color: #0e76a8;
  border: 1px solid white;
  border-radius: 3px;
  color: #231E39;
  font-family: Montserrat, sans-serif;
  font-weight: 500;
  padding: 10px 25px;
}

.test:hover {
  background-color: transparent;
  color: white;
  }
/*.test:focus {
    border: red;
    color: white;
    background-color: lightblue;
    box-shadow: none;
    outline: none;
}*/
</style>
