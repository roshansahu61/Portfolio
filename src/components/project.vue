<template>
  <section>
    <p id="project" class="section__text__p1 text-center mt-5">Have a look at </p></p>
    <h1 class="title text-center mb-5"> My Projects</h1>
    
    <div class="container">
      <VueSlickCarousel
        :arrows="true" 
        :dots="true"
        :infinite = "true"
        :slidesToShow= "3" 
        :slidesToScroll="1"
        :autoplay= "true"
        :speed="2000"
        :autoplaySpeed="2000"
      >
        <div class="project-image">
          <div>
            <img src="../assets/blood_project.png"/>
          </div>
          <button class="btn btn-outline-info" @click="viewUrl('https://drive.google.com/file/d/1EAc3rqqnCm4HFRsbnDYhI07FVBPTMlOd/view?usp=sharing')">
            View
          </button>
          <button class="btn btn-outline-info ml-3" @click="viewUrl('https://github.com/arjad/Blood-web')">
            Code
          </button>
        </div>
        <div class="project-image">
          <div>
            <img src="../assets/amazon_project.png"/>
          </div>
          <button class="btn btn-outline-info" @click="viewUrl('https://optimistic-shockley-06ae03.netlify.app/')">
            View
          </button>
          <button class="btn btn-outline-info ml-3" @click="viewUrl('https://github.com/arjad/Amazon-Clone')">
            Code
          </button>
        </div>
        <div class="project-image">
          <div>
            <img src="../assets/forest_project.png"/>
          </div>
          <button class="btn btn-outline-info ml-3" @click="viewUrl('https://ecstatic-noether-654f18.netlify.app/')">
            View
          </button>
          <button class="btn btn-outline-info ml-3" @click="viewUrl('https://github.com/arjad/Forest-Project')">
            Code
          </button>
        </div>
        <div class="project-image">
          <div>
            <img src="../assets/restaurant_project.png"/>
          </div>
          <button class="btn btn-outline-info" @click="viewUrl('https://kaleidoscopic-cat-37f8fc.netlify.app/')">
            View
          </button>
          <button class="btn btn-outline-info ml-3" @click="viewUrl('https://github.com/arjad/food-menu')">
            Code
          </button>
        </div>
      </VueSlickCarousel>
    </div>
  </section>
</template>

<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
 
  export default {
    name: 'MyComponent',
    components: { VueSlickCarousel },
    methods: {
      viewUrl(url) {
        window.location.href = url;
      }
    }
  }
</script>

<style scoped lang="scss">
.project-image {
  width:5vh;
  margin:10px;

  div {
    padding: 1rem;
    position: relative;
    
    img { 
      height: 100%;
      width: 100%;
    }
  }
}
</style>