<template>
  <!-- HTML SECTION -->
  <div id="app">
      <nav-bar/>

      <div class="hero">
        <div class="hero-icon">
        </div>
      </div>


      <div class="roller">
        <div class="spoke"/>
        <div class="spoke"/>
        <div class="spoke"/>
        <div class="spoke"/>
        <div class="roller-ct"/>
      </div>

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

/* ROLLER */
.roller {
  width: 80px; 
  height: 80px;
  position: absolute;
  z-index: 10;
  border-radius: 50%;
  background-color: black;
  /*-webkit-animation: roll-ball 5s infinite; /* Safari 4.0 - 8.0 */
  animation-name: rollball;
  animation-duration: 5s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  border: 16px solid #666;
}

.roller-ct {
  width: 40px;
  height: 40px;
  left: 12.5%;
  margin-top: 10px;
  border-radius: 50%;
  background-color: #ccc;
  border: 10px solid #eee;
  z-index: 100;
  position: absolute;
}

@keyframes rollball {
  from {
    left: -120px;
    top: 665px;
  }
  to {
    left: calc(100% + 40px);
    top: calc((.08748866 * (100vw + 140px) ) + 665px);
  }
}

.spoke {
  width: 12px;
  height: 80px;
  position: absolute;
  left: 35px;
  background-color: #ccc;
  animation: rotate-ball 2.5s infinite;
  animation-timing-function: linear;
}

.spoke:nth-child(2) {
  animation: rotate-ball2 2.5s infinite;
  animation-timing-function: linear;
} 
.spoke:nth-child(3) {
  animation: rotate-ball3 2.5s infinite;
  animation-timing-function: linear;
} 
.spoke:nth-child(4) {
  animation: rotate-ball4 2.5s infinite;
  animation-timing-function: linear;
} 

/*@-webkit-keyframes rollball {
  from {
    left: -120px;
    top: 665px;
  }
  to {
    left: calc(100% + 40px);
     top: calc((.08748866 * (100vw + 140px) ) + 665px);
  }
}*/

@keyframes rotate-ball {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}

@keyframes rotate-ball2 {
  from {
    transform: rotate(45deg);
  }
  to {
    transform: rotate(404deg);
  }
}

@keyframes rotate-ball3 {
  from {
    transform: rotate(90deg);
  }
  to {
    transform: rotate(449deg);
  }
}

@keyframes rotate-ball4 {
  from {
    transform: rotate(135deg);
  }
  to {
    transform: rotate(494deg);
  }
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
