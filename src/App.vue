<template>
  <div id="app" :class="{ 'dark-mode': darkMode }">
    <Nav />
    <Summary />
    <About />
    <Skills />
    <Project/>
    <Contact />
    <CanvasAnimation />

    <button
      id="back-to-top"
      class="p-3 rounded-circle"
      v-show="isScrollDown"
      @click="scrollToTop"
    >
      <i class="fas fa-arrow-up"></i>
    </button>
  </div>
</template>

<script>
import Nav from "./components/nav.vue";
import Summary from "./components/summary.vue";
import About from "./components/about.vue";
import Skills from "./components/skills.vue";
import Project from "./components/project.vue";
import Contact from "./components/contact.vue";
import CanvasAnimation from "./components/features/canvas.vue";
import { onMounted } from "vue";
import AOS from "aos";

export default {
  components: {
    Nav,
    Summary,
    About,
    Skills,
    Project,
    Contact,
    CanvasAnimation,
  },
  data() {
    return {
      isScrollDown: false,
      darkMode: sessionStorage.getItem('darkMode') === 'true',
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      } );
    },
    handleScroll() {
      this.isScrollDown = window.scrollY > 0;
    },
  },
  mounted() {
    Zoomtastic.mount({
      size: '95%',
      easing: 'ease',
      duration: 300,
      background: 'rgba(0, 0, 0, 0.9)',
      filter: 'drop-shadow(0 2px 16px rgba(0, 0, 0, 0.3))',
      animation: 'slide'
    });

    Zoomtastic.listen('[zoomtastic]', 'src');
    window.addEventListener("scroll", this.handleScroll);


    AOS.init();
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style lang="scss">
* { 
  margin: 0;
  padding: 0;
  font-family: "Segoe UI", Tahoma;
  transition: width 1s ease, height 1s ease, background-color 1s ease;

}
::-webkit-scrollbar {
  width: 15px;
}
::-webkit-scrollbar-thumb {
  background: #888; 
  border-radius: 10px;
}
::selection {
  background-color: lightgrey;
}

#back-to-top {
  position: fixed;
  bottom: 35px;
  right: 35px;
  padding: 1rem;
  background-color: #333;
  color: #fff;
  border: none;
  cursor: pointer;
  transition: opacity 0.3s ease-in-out;
  &:hover {
    opacity: 0.8;
  }
}

.dark-mode {
  background: black;
  color:white;
  #navigation{
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.5) !important;
  }
  .vue-typer {
    .custom.char {
      color: white;
    }
  }
  .btn, .btn-color-2{
    color: white !important;
  }

  .footer {
    background: linear-gradient(to top, rgba(18, 41, 115, 1) 40%, rgba(53, 134, 255, 1) 80%);
  }
}


</style>
