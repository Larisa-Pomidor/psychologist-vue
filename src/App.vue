<template>
  <Header />
  <Home />
  <Footer />
  <Sidebar />
</template>

<script>
import Header from './components/Header.vue'
import Home from './components/Home.vue'
import Footer from './components/Footer.vue'
import Sidebar from './components/Sidebar.vue'

export default {
  name: 'App',
  components: {
    Header,
    Home,
    Footer,
    Sidebar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Pattaya&family=Poiret+One&display=swap');

*,
*:after,
*:before {
  box-sizing: border-box;
}

html,
body {
  margin: 0;
  padding: 0;
  color: black;
  font-family: 'Poiret One', cursive;
}

.container {
  max-width: 1240px;
  margin: auto;
}

@media(max-width: 900px) {
  .container {
    padding: 0 20px;
  }
}
</style>
