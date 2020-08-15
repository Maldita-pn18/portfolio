<template>
  <div class="container-fluid nopadding">
    <div class="col-sm-12 nopadding">
      <b-navbar toggleable="lg" type="dark" variant="info" class="navs" fixed="top">
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item @click="redirect('/')">Home</b-nav-item>
            <b-nav-item @click="redirect('/about')">About</b-nav-item>
            <b-nav-item>Resume`</b-nav-item>
            <b-nav-item @click="redirect('/project')">Projects</b-nav-item>
            <b-nav-item @click="redirect('/contact')">Contact</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <div id="app">
      <router-view/>
    </div>
  </div>
</template>
<script>
import router from './router'
export default {
  data () {
    return {}
  },
  methods: {
    redirect (url) {
      router.push(url)
    }
  }
}
</script>
<style scoped>
.navs {
  background: linear-gradient(45deg, #0e76a8, #c648c8) !important;
  font-size: 18px;
}
.navbar-dark .navbar-nav .nav-link {
  color: white !important;
}
.navbar-dark .navbar-nav .nav-link:hover {
  color: black !important;
}
#about {
  color: black !important;
}
.nopadding {
  padding: 0px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
