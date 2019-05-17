<template>
  <!-- HTML SECTION -->
  <div id="app">
      <nav-bar/>

      <div class="hero">
        <div class="hero-icon">
        </div>
      </div>

      <jeep/>
      <div class="bio">
        <div class="greeting">
          <h2>Hi, I'm Jake. Nice to meet you.</h2>
          <p>I have worn a few hats in my day including affiliate marketer, 3D artist and animator, and now full time developer, and more.  Regardless of the job, I always find myself happiest when I can fulfill my own creativity and help others succeed. Let's talk about what I can to do help you grow your business and achieve your goals!</p>
        </div>
      </div>


      <div class="skill-container">
        <div class="skills">
        </div>
      </div>

    </div>
  </div>
</template>



<script>
// JAVASCRIPT SECTION
import Jeep     from './components/jeep/Jeep.vue';
import NavBar   from './components/nav/NavBar.vue';

export default {
  name: 'app',
  components: {
    Jeep,
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

html, body{
  max-width: 100%;
  overflow-x: hidden;
  font-family: 'Karla', sans-serif;
}

h1,h2,h3,h4,h5,h6 {
  padding: 20px;

}
h1, h2 {
  font-family: 'Fjalla One', sans-serif;
}

.container {
  max-width: 992px;
  margin: 0 auto;
}

.hero {
  width: 100%;
  padding: 20px 0 140px;
}

.hero-icon {
  width: 260px;
  height: 260px;
  border-radius: 50%;
  background-color: #444488;
  border: 20px solid #8888FF;
  margin: 0 auto;
}

/* BIO */
.bio {
  display: block;
  width: 100%;
  height: 600px;
  background-image: linear-gradient(#3030bf, #406dff);
}

.bio:before {
  content: "";
  display: block;
  width: 100%;
  height: 100%;
  background: white;
  transform-origin: top right;
  -ms-transform: skew(85deg, 0deg);
  -webkit-transform: skew(85deg, 0deg);
  transform: skew(85deg, 0deg);
  backface-visibility: hidden;
  -ms-backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  position: absoute;
  z-index: -100;
}

.greeting {
  text-align: center;
  color: white;
  margin: -400px auto 0;
  max-width: 600px;
}

.greeting h2 {
  font-size: 32px;
}

.greeting p {
  font-size: 18px;
  line-height: 1.6;
}

.skill-container {
  padding: 20px;
}

.skills {
  max-width: 992px;
  height: 400px;
  margin: -60px auto 0;
  z-index: 1;
  left: calc((100% - 992px) / 2);
  background-color: white;
  border: 1px solid #d0d0ff;
  border-radius: 20px;
}

</style>
