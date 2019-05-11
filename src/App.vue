<template>
  <!-- HTML SECTION -->
  <div id="app">
      <nav-bar/>

      <div class="image">

      </div>
      <div class="hero">

      </div>
      <div class="bio">
      </div>
    </div>
  </div>
</template>



<script>
// JAVASCRIPT SECTION
import NavBar from './components/nav/NavBar.vue';

export default {
  name: 'app',
  components: {
    NavBar
  },
  data () {
    return {
      
    };
  }
}
</script>



<style>
/* CSS SECTION */

* { padding: 0; margin: 0;}

html {
  font-family: 'Karla', sans-serif;
}

h1,h2,h3,h4,h5,h6 {
  padding: 20px;

}
h1 {
  font-family: 'Fjalla One', sans-serif;
}

.container {
  max-width: 992px;
  margin: 0 auto;
}

.image {
  width: 100%;
  height: 600px;
}
.hero {
  width: 992px;
  height: 400px;
  margin: 0 auto;
  position: absolute;
  z-index: 100;
  left: calc((100% - 992px) / 2);
  background-color: white;
  border: 4px solid #d0d0ff;
  border-radius: 20px;
}

/* BIO */
.bio {
  margin-top: 60px;
  display: block;
  width: 100%;
  height: 500px;
  background-color: #4040ff;
}

.bio:after {
    content: " ";
    display: block;
    /* position: absolute; */
    /* z-index: -1; */
    width: 100%;
    height: 100%;
    top: 0;
    right: 0;
    background: white;
    transform-origin: top right;
    -ms-transform: skew(85deg, 0deg);
    -webkit-transform: skew(85deg, 0deg);
    transform: skew(85deg, 0deg);
    -webkit-backface-visibility: hidden;
}

</style>
