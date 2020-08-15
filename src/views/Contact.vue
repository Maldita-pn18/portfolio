<template>
    <div class="container-fluid">
        <center>
            <div class="card-container">
                <form>
                <h3>• Be in touch •</h3>
                <br>
                <input id="name" placeholder="Name" type="text" name="name" required="required" value>
                <input
                    id="email"
                    placeholder="Enter email"
                    type="email"
                    name="email"
                    required="required"
                    value
                >
                <textarea placeholder="Enter your message"></textarea>
                <br>
                <button id="send" class="button" type="submit">Submit</button>
                </form>
            </div>
        </center>
    </div>
</template>

<script>
export default {}
</script>

<style scoped>
.contact {
  color: white;
  text-align: center;
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
  font-size: calc(20vw / var(--char-total));
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

h3 {
  font-size: 30px;
  background: -webkit-linear-gradient(#eee, #333);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.card-container {
  background-color: #231e39;
  border-radius: 5px;
  border: 1px solid white;
  box-shadow: 0px 10px 20px -10px rgba(0, 0, 0, 0.75);
  color: #b3b8cd;
  padding-top: 30px;
  position: relative;
  width: 500px;
  height: 500px;
  max-width: 100%;
  text-align: center;
  padding-left: 20px;
  padding-right: 20px;
  position: absolute !important;
  top: 50% !important;
  left: 50% !important;
  margin-right: -50% !important;
  transform: translate(-50%, -50%) !important;
}
.card-container .round {
  background-color: #1f1a36;
  text-align: left;
  padding: 15px;
  margin-top: 30px;
}
input,
textarea {
  width: 100%;
  height: 50%;
  background-color: #1f1a36;
  margin-top: 30px;
  border: 1px solid #2d2747;
  border-radius: 3px;
  display: inline-block;
  font-size: 13px;
  margin: 0 7px 7px 0;
  padding: 10px;
  box-sizing: border-box;
}

textarea {
  height: 200px;
  resize: none;
  overflow: auto;
}

input:focus,
textarea:focus {
  color: white;
}

.button {
  background-color: #0e76a8;
  border: 1px solid white;
  border-radius: 3px;
  color: white;
  font-family: Montserrat, sans-serif;
  font-weight: 500;
  padding: 10px 25px;
}

.button:hover {
  background-color: transparent;
  color: white;
}
</style>
