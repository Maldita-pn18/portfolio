<template>
  <div class="container-fluid">
    <div class="main">
      <div class="box" v-for="( element, index) in rowProjects[0]" :key="index">
        <img :src="element">
        <div class="overlay"></div>
        <!-- <a class="more" data-toggle="modal" v-b-modal.rowProjects[1][index]>Read more</a> -->
        <b-button v-b-modal.rowProjects[1][index]>{{rowProjects[1][index]}}</b-button>
      </div>
    </div>
    <div>
        <br>
        <br>
        <br>
        <b-button v-b-modal.modal-1>Launch demo modal</b-button>
        <b-modal id="modal-1" title="BootstrapVue">
            <p class="my-4">Hello from modal! asdf</p>
        </b-modal>
    </div>
    <b-modal id="myModal1" class="modal card-container">
        <div class="card">
            <div class="col-sm-12 text-right">
                <a data-dismiss="modal" style="font-size: 15px">X</a>
            </div>
            <img class="card-img-top" :src="require('../assets/bus.png')" alt="Card image cap">
            <div class="card-body">
                <h1>LinkOD</h1>
                <h4>Bus Reservation System</h4>
                <p>A web application that will allocate seats to passengers and can reserve bus tickets digitally.</p>
            </div>
          <br>
        </div>
        <br>
        <p>TOOLS:</p>
        <ul>
            <li>ReactJs</li>
            <li>Node-Express</li>
            <li>NoSql (MongoDB)</li>
        </ul>
        <div class="col-sm-12 text-right">
            <a href="https://github.com/Maldita-pn18/jailmanagement">
                <i class="fa fa-github hub"></i>
            </a>
        </div>
    </b-modal   >
    <div id="myModal2" class="modal card-container">
        <div class="card">
            <div class="col-sm-12 text-right">
             <a data-dismiss="modal" style="font-size: 15px">X</a>
            </div>
            <img class="card-img-top" :src="require('../assets/jims.png')" alt="Card image cap">
            <div class="card-body">
                <h1>JIMS</h1>
                <h4>Jail Information Management System</h4>
                <p>Jail Management products are designed to help agencies efficiently track and process inmate's visitors from booking.</p>
            </div>
            <br>
        </div>
        <br>
        <p>TOOLS:</p>
        <ul>
            <li>Angular</li>
            <li>Node-Express</li>
        </ul>
        <div class="col-sm-12 text-right">
            <a href="https://github.com/Maldita-pn18/linkod">
            <i class="fa fa-github hub"></i>
            </a>
        </div>
    </div>
    <div id="myModal3" class="modal card-container">
        <div class="card">
            <div class="col-sm-12 text-right">
                <a data-dismiss="modal" style="font-size: 15px">X</a>
            </div>
            <img class="card-img-top" :src="require('../assets/mqtt.png')" alt="Card image cap">
            <div class="card-body">
                <h1>MQTT</h1>
                <h4>MQTT Website Application</h4>
                <p>The web app connects using MQTT as the transport protocol, running over WebSockets. MQTT for clients is in the subscription of MQTT data from a server that retrieves and displays node data.</p>
            </div>
            <br>
        </div>
        <br>
        <p>TOOLS:</p>
        <ul>
            <li>Node-Express</li>
        </ul>
        <div class="col-sm-3 text-right">
            <a href="https://maldita-pn18.github.io/">View Site</a>
        </div>
        <div class="col-sm-9 text-right">
            <a href="https://github.com/Maldita-pn18/Maldita-pn18.github.io">
                <i class="fa fa-github hub"></i>
            </a>
        </div>
      </div>
      <div id="myModal4" class="modal card-container">
            <div class="card">
                <div class="col-sm-12 text-right">
                    <a data-dismiss="modal" style="font-size: 15px">X</a>
                </div>
                <img class="card-img-top" :src="require('../assets/chat.png')" alt="Card image cap">
                <div class="card-body">
                    <h1>WeChat</h1>
                    <h4>A Chat Application</h4>
                    <p>Communication channel between a client and a server. This means that the server can push messages to clients.</p>
                </div>
                <br>
            </div>
            <br>
            <p>TOOLS:</p>
            <ul>
                <li>Socket.io</li>
                <li>Node-Express</li>
            </ul>
            <div class="col-sm-3 text-right">
            <a href="https://heroku-mgc.herokuapp.com/">View Site</a>
            </div>
            <div class="col-sm-9 text-right">
            <a href="https://github.com/Maldita-pn18/heroku-node-cordoto">
                <i class="fa fa-github hub"></i>
            </a>
            </div>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      rowProjects: [
        [
          require('../assets/react.jpg'),
          require('../assets/angular.png'),
          require('../assets/nodejs.jpg'),
          require('../assets/nodeio.png')
        ],
        ['myModal1', 'myModal2', 'myModal3', 'myModal4']
      ]
    }
  }
}
</script>
<style scoped>
.main {
  position: absolute !important;
  top: 15% !important;
  left: 10% !important;
  margin-right: 10% !important;
}
.box {
  width: 280px;
  height: 230px;
  border: 2px solid #000;
  border-radius: 2px;
  float: left;
  margin: 20px 30px;
}

.box img {
  width: 300px;
  height: 250px;
}

.box .overlay {
  width: 300px;
  height: 250px;
  background: #fff;
  margin: -250px 0px 0px 0px;
  opacity: 0.5;
}

.box a {
  padding: 5px 7px;
  border: 1px solid #000;
  text-decoration: none;
  font-family: sans-serif;
  font-size: 14px;
  margin: -140px 0px 0px 15px;
  display: inline-block;
  opacity: 0;
  transition: all 0.5s ease-in-out;
  cursor: pointer; /* z-index: 10000; */
  position: absolute;
}

.box .overlay:hover {
  opacity: 0.1;
  transition: all 0.5s ease-in-out;
  width: 300px;
  margin-left: 50px;
  float: right;
}

.box:hover {
  box-shadow: 0px 0px 10px #6a6a6a;
  border: 1px solid #00dfdf;
  transition: all 0.5s ease-in-out;
}

.box:hover a {
  opacity: 1;
  background: #ffffff;
  color: #000000;
  margin: -40px 0px 0px 15px;
  border-radius: 1px;
}

.box a:hover {
  border: 1px solid #00dfdf;
  transition: all 0.5s ease-in-out;
}
img {
  width: 60%;
  height: 60%;
}
h1 {
  background: linear-gradient(45deg, #0e76a8, #c648c8);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
p {
  text-align: justify;
  text-justify: inter-word;
  margin: 20px;
}
.card-container {
  background-color: #231e39;
  border-radius: 5px;
  border: 1px solid white;
  box-shadow: 0px 10px 20px -10px rgba(0, 0, 0, 0.75);
  color: #b3b8cd;
  padding-top: 30px;
  position: center;
  width: 500px;
  height: 650px;
  max-width: 100%;
  text-align: center;
  margin: auto;
}
ul {
  text-align: left;
}
.hub {
  font-size: 30px;
}
</style>
