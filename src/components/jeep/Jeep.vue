<template>
	<div class="jeep">
		<div class="spare-tire"/>
		<div class="jeep-back"/>
		<div class="jeep-main"/>
		<div class="jeep-front"/>
		<div class="window back-window"/>
		<div class="window mid-window"/>
		<div class="window front-window"/>
		<div class="wheel back-wheel">
	        <div class="spoke"/>
	        <div class="spoke"/>
	        <div class="spoke"/>
	        <div class="spoke"/>
	        <div class="wheel-ct"/>
	    </div>
	    <div class="wheel front-wheel">
	        <div class="spoke"/>
	        <div class="spoke"/>
	        <div class="spoke"/>
	        <div class="spoke"/>
	        <div class="wheel-ct"/>
	    </div>
	</div>
</template>


<style scoped>

div {
	position: absolute;
}

.jeep {
	top: 300px;
	left: 100px;
	animation-name: drive;
  	animation-duration: 5s;
  	animation-iteration-count: infinite;
  	animation-timing-function: linear;
  	transform: rotate(5deg);
  	z-index: 1;
}

.spare-tire {
	width: 15px;
	height: 50px;
	border-radius: 8px;
	background-color: #333;
	margin-left: -14px;
	margin-top: 30px;
	transform: rotate(2deg);
}

/* JEEP MAIN */
.jeep-main {
	width: 160px;
	height: 100px;
	transform: skewX(20deg);
	background-color: #222;
	border-radius: 6px;
	margin-left: 20px;
}

.jeep-back {
	width: 60px;
	height: 100px;
	background-color: #222;
	transform: skewX(-3deg);
	border-radius: 6px;
}

.jeep-front {
	width: 180px;
	height: 60px;
	transform: skewX(20deg);
	background-color: #222;
	border-radius: 10px;
	margin-left: 80px;
	margin-top: 40px;
}

.window {
	width: 40px;
	height: 30px;
	background-color: lightblue;
	margin-top: 10px;
}

.back-window {
	margin-left: 15px;
}

.mid-window {
	margin-left: 65px;
}

.front-window {
	height: 0;
	width: 40px;
	margin-left: 115px;
	border-style: solid;
	border-color: #222 #222 lightblue #222;
	border-width: 0 10px 30px 0;
}


/* WHEELS */
.wheel {
  width: 40px; 
  height: 40px;
  z-index: 10;
  margin-top: 70px;
  border-radius: 50%;
  background-color: black;
  /*-webkit-animation: roll-ball 5s infinite; /* Safari 4.0 - 8.0 */
  border: 8px solid #666;
}

.wheel-ct {
  width: 12px;
  height: 12px;
  margin-top: 9px;
  margin-left: 9px;
  border-radius: 50%;
  background-color: #ccc;
  border: 5px solid #eee;
  z-index: 100;
}

.back-wheel {
	margin-left: 10px;
}

.front-wheel {
	margin-left: 200px;
}

@keyframes drive {
  from {
    left: -300px;
    top: 645px;
  }
  to {
    left: calc(100% + 40px);
    top: calc((.08748866 * (100vw + 300px) ) + 645px);
  }
}

@-webkit-keyframes drive {
  from {
    left: -120px;
    top: 645px;
  }
  to {
    left: calc(100% + 40px);
     top: calc((.08748866 * (100vw + 300px) ) + 645px);
  }
}

.spoke {
  width: 8px;
  height: 40px;
  margin-left: 16px;
  background-color: #ccc;
  animation: rotate-wheel 2.5s infinite;
  animation-timing-function: linear;
}

.spoke:nth-child(2) {
  animation: rotate-wheel2 2.5s infinite;
  animation-timing-function: linear;
} 
.spoke:nth-child(3) {
  animation: rotate-wheel3 2.5s infinite;
  animation-timing-function: linear;
} 
.spoke:nth-child(4) {
  animation: rotate-wheel4 2.5s infinite;
  animation-timing-function: linear;
} 



@keyframes rotate-wheel {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}

@keyframes rotate-wheel2 {
  from {
    transform: rotate(45deg);
  }
  to {
    transform: rotate(404deg);
  }
}

@keyframes rotate-wheel3 {
  from {
    transform: rotate(90deg);
  }
  to {
    transform: rotate(449deg);
  }
}

@keyframes rotate-wheel4 {
  from {
    transform: rotate(135deg);
  }
  to {
    transform: rotate(494deg);
  }
}
</style>