<template>
  <div class="container-fluid aboutpage">
    <div class="row">
      <div class="col-sm-3 card-container aboutpageSection">
        <img class="round" :src="require('../assets/picture.jpg')" alt="user">
        <h3>Mary Grace Cordoto</h3>
        <br>
        <p class="qoute"><i>"An expert in anything was once a beginner"</i></p>
        <h6>Passerelles Numeriques Scholar</h6>
        <p>Web developer</p>
        <br>
        <ul class="social-icons">
          <li>
            <a href="https://google.com/">
              <i class="far fa-envelope"></i>
            </a>
          </li>
          <li>
            <a href="https://www.linkedin.com/in/marygrace-cordoto-45760a195/">
              <i class="fab fa-linkedin"></i>
            </a>
          </li>
          <li>
            <a href="https://github.com/Maldita-pn18">
              <i class="fab fa-github"></i>
            </a>
          </li>
        </ul>
        <div class="row text-center">
          <div class="col-sm-6">
            <img class="skillLogo aboutlogo" :src="require('../assets/pn.png')" />
            <p class="word">Passerelles Numeriques</p>
          </div>
          <div class="col-sm-6">
            <img class="skillLogo aboutlogo" :src="require('../assets/usc.png')" />
            <p class="word"> Univesity of San Carlos</p>
          </div>
        </div>
      </div>
      <div class="col-sm-9">
        <div class="col-sm-9card skillsSection">
          <div class="card-header text-left skillsHeader">
            SKILLS
          </div>
          <div class="col-sm-12 logopadding">
            <div class="row logopadding">
              <div class="col-sm-3 logopadding" v-for="( element, index ) in row1[0]" :key="index">
                <img class="skillLogo" :src="element" alt="user">
                <p :style="skillLabel">{{ row1[1][index] }}</p>
              </div>
            </div>
            <div class="row logopadding">
              <div class="col-sm-3 logopadding" v-for="( element, index) in row2[0]" :key="index">
                <img class="skillLogo" :src="element" alt="user">
                <p :style="skillLabel">{{ row2[1][index] }}</p>
              </div>
            </div>
          </div>
          <center>
            <div class="buttons">
              <button id="contact" class="primary contactBTN" @click="redirect('/contact')">Contact</button>
            </div>
          </center>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import router from '../router'
export default {
  data () {
    return {
      row1: [
        [require('../assets/React.webp'), require('../assets/angular.png'), require('../assets/node.png'), require('../assets/python.png')],
        ['ReactJs', 'Angular', 'NodeJs', 'Python']
      ],
      row2: [
        [require('../assets/java.png'), require('../assets/css3.png'), require('../assets/html.png'), require('../assets/js.png')],
        ['Java', 'CSS', 'HTML', 'JAVASCRIPT']
      ],
      skillLabel: 'color: white;'
    }
  },
  methods: {
    redirect (url) {
      router.push(url)
    }
  }
}
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Baloo+Paaji+2:wght@400;500&display=swap");
@import url("https://fonts.googleapis.com/css?family=Open+Sans:700");
* {
  box-sizing: border-box;
}
.about {
  color: white;
  text-align: center;
}
.qoute{
  font-size: 13px;
}
.aboutpage {
  background: #231e39;
}
.skillLogo {
  height: 120px !important;
  width: 120px;
  padding: 20px;
  border-bottom: 1px solid white;
  border-radius: 0px;
}
.word{
  font-size: 11px;
}
.skillsHeader{
  color: white;
  font-size: 30px;
  border-left: 10px solid #d900ff;
  margin-bottom: 100px;
}
.skillsSection {
  padding: 0px;
  background: transparent;
  border-radius: 3px;
  margin-top: 100px;
  padding-bottom: 100px;
}
.aboutpageSection{
  margin-top: 100px;
}
.buttons{
  margin-top: 100px;
}
.logopadding{
  padding: 0px !important;
}

html {
  display: flex;
}

body {
  background-color: #28223f;
  font-family: Montserrat, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  min-height: 100vh;
  margin: 0;
  margin: auto;
}
.alrazy-title {
  font-family: Helvetica;
  font-size: calc(15vw / var(--char-total));
  position: relative;
  padding: 0.2em 0;
  overflow: hidden;
}

.alrazy-title:after {
  content: "";
  display: block;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  border-bottom: solid 0.2em;
  -webkit-animation: underline 1s cubic-bezier(0.8, 0, 0, 1);
  animation: underline 1s cubic-bezier(0.8, 0, 0, 1);
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}

@-webkit-keyframes underline {
  from {
    -webkit-transform: scaleX(0);
    transform: scaleX(0);
  }
}

@keyframes underline {
  from {
    -webkit-transform: scaleX(0);
    transform: scaleX(0);
  }
}

.alrazy-title .word {
  display: inline-block;
  -webkit-animation: slide-up 1.25s cubic-bezier(0.5, 0.2, 0, 1);
  animation: slide-up 1.25s cubic-bezier(0.5, 0.2, 0, 1);
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  -webkit-animation-delay: calc(0.1s + (0.1s * var(--word-index)));
  animation-delay: calc(0.1s + (0.1s * var(--word-index)));
}

@-webkit-keyframes slide-up {
  from {
    -webkit-transform: translateY(50%);
    transform: translateY(50%);
  }
}

@keyframes slide-up {
  from {
    -webkit-transform: translateY(50%);
    transform: translateY(50%);
  }
}

.splitting-mark {
  color: #fff !important;
}

h2 {
  color: white;
}
h3 {
  margin: 10px 0;
}

h6 {
  margin: 5px 0;
  text-transform: uppercase;
}

p {
  font-size: 14px;
  line-height: 21px;
}

.card-container {
  background-color: #231e39;
  border-radius: 0px;
  border-right: 1px solid white;
  box-shadow: 0px 10px 20px -10px rgba(0, 0, 0, 0.75);
  color: #b3b8cd;
  padding-top: 30px;
  padding-left: 5px;
  padding-right: 5px;
  position: relative;
  width: 100%;
  max-width: 100%;
  text-align: center;
}

.card-container .round {
  border: 1px solid #03bfcb;
  border-radius: 50%;
  padding: 7px;
  height: 190px;
  width: 190px;
}

.contactBTN {
  background-color: transparent;
  border: 1px solid white;
  border-radius: 3px;
  color: white;
  font-family: Montserrat, sans-serif;
  font-weight: 500;
  padding: 10px 25px;
  width: 260px;
}

.contactBTN:hover {
  background-color: #044ac4;
  color: white;
}

.social-icons {
  padding: 0;
  list-style: none;
  margin: 1em;
}

.social-icons li {
  display: inline-block;
  margin: 0.15em;
  position: relative;
  font-size: 35px;
  margin: 10px;
}
.social-icons li :hover{
  color:#d900ff;
}
.skills {
  background-color: #1f1a36;
  text-align: left;
  padding: 15px;
  margin-top: 30px;
}
.skills ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.skills ul li {
  border: 1px solid #2d2747;
  border-radius: 2px;
  display: inline-block;
  font-size: 12px;
  margin: 0 7px 7px 0;
  padding: 7px;
}
@media (min-width: 576px){
 .aboutlogo{
   height: 90px !important;
   width: 90px !important;
 }
}
@media (min-width: 1000px){
 .aboutlogo{
   height: 120px !important;
   width: 120px !important;
 }
}
@media (max-width: 575px){
 .aboutlogo{
   height: 120px !important;
   width: 120px !important;
 }
}
</style>
