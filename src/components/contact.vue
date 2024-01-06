<template>
  <footer id="contact" class="footer d-flex justify-content-center alig-item-center">
    <div class="waves">
      <div class="wave" id="wave1"></div>
      <div class="wave" id="wave2"></div>
      <div class="wave" id="wave3"></div>
      <div class="wave" id="wave4"></div>
    </div>
    <div class="text-center">
      <p class="section__text__p1">Want To Get in Touch</p>
      <h1 class="title">Contact Me</h1>
    </div>
    <ul class="social-icon container">
      <li class="social-icon__item">
        <a class="social-icon__link" href="https://www.linkedin.com/in/arjad/" target="_blank">
          <i class="fa-brands fa-linkedin icon"></i>
          <span class="pl-2"> https://www.linkedin.com/in/arjad/ </span>
        </a>
      </li>
      <li class="social-icon__item">
        <a class="social-icon__link" href="https://github.com/arjad" target="_blank">
          <i class="icon fa-brands fa-github"></i>
          <span class="pl-2"> https://github.com/arjad </span>
        </a>
      </li>
      <li class="social-icon__item">
        <a class="social-icon__link" href="mailto:arjadgohar14@gmail.com">
          <i class="fa-solid fa-envelope"></i>
          <span class="pl-2">arjadgohar14@gmail.com </span>
        </a>
      </li>
      <li class="social-icon__item">
        <a class="social-icon__link" href="tel:+923024466257">
          <i class="fa-solid fa-phone"></i>
          <span class="pl-2"> +92302-4466257 </span>
        </a>
      </li>
      <li class="social-icon__item">
        <a class="social-icon__link" href="javascript:void(0)">
          <i class="fa-solid fa-house"></i>
          <span class="pl-2"> House No 293 Chauburji Park, Lahore, Paksitan. </span>
        </a>
      </li>
    </ul>
    
    <p class="text-white text-right pr-3"> 
      This Project is made with <b>Vue JS</b>
      <button class="cursor" onclick="location.href=''"> View Code here </button>
    </p>
  </footer>
</template>

<script>
</script>

<style lang="scss" scoped>
.footer {
  position: relative;
  width: 100%;
  background: #3586ff;
  flex-direction: column;
  margin-top: 25vh;
  color: white;
}

.social-icon{
  position: relative;
}

.social-icon__item{
  list-style: none;
  padding-top: 15px;
}

.social-icon__link {
  color: #fff;
  margin: 0 10px;
  display: inline-block;
  transition: 0.5s;
  i {
    font-size: 1.5rem;
  }
}
.social-icon__link:hover {
  transform: translateY(-10px);
}

.wave {
  position: absolute;
  top: -100px;
  left: 0;
  width: 100%;
  height: 100px;
  background: url("https://i.ibb.co/wQZVxxk/wave.png");
  background-size: 1000px 100px;
}

.wave#wave1 {
  z-index: 1000;
  opacity: 1;
  bottom: 0;
  animation: animateWaves 4s linear infinite;
}

.wave#wave2 {
  z-index: 999;
  opacity: 0.5;
  bottom: 10px;
  animation: animate 4s linear infinite !important;
}

.wave#wave3 {
  z-index: 1000;
  opacity: 0.2;
  bottom: 15px;
  animation: animateWaves 3s linear infinite;
}

.wave#wave4 {
  z-index: 999;
  opacity: 0.7;
  bottom: 20px;
  animation: animate 3s linear infinite;
}

@keyframes animateWaves {
  0% {
    background-position-x: 1000px;
  }
  100% {
    background-positon-x: 0px;
  }
}

@keyframes animate {
  0% {
    background-position-x: -1000px;
  }
  100% {
    background-positon-x: 0px;
  }
}

</style>
