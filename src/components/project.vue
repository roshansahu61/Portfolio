<template>
  <section id="projects">
    <Heading :title="'My Projects'" :subtitle="'Have a look at'" />

    <section class="project-container container-fluid">
      <div v-for="(project, index) in projects" :key="index" class="card px-0">
        <img :src="project.image" class="card-img-top" :alt="project.title"/>

        <div class="card-body shadow">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
            <div class="mb-3">
              <span v-for="(tech, i) in project.technologies" :key="i" class="badge rounded-pill px-3 py-2 mx-2 border border-dark">
                {{ tech }}
              </span>
            </div>
            <div class="d-flex">
                <a :href="project.github" target="_blank" class="btn me-2">
                  <i class="fa-brands fa-github mr-2"></i>GitHub
                </a>
                <a :href="project.live" target="_blank" class="btn">
                  <i class="fa-solid fa-arrow-up-right-from-square"></i>  Live Demo
                </a>
            </div>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  import Heading from "./common/heading.vue";
 
  export default {
    name: 'MyComponent',
    components: { VueSlickCarousel, Heading },
    methods: {
      viewUrl(url) {
        window.location.href = url;
      }
    },
    data() {
      return {
        projects: [
          {
            title: "Blood Donation Website",
            description: "A real-time chat system for fast and responsive communication.",
            image: "/projects/project_blood_web.png",
            live: "https://dreamy-banoffee-b9dd62.netlify.app/",
            github: "https://github.com/arjad/Blood-web",
            technologies: ["React JS", "Node JS", "Mongo DB"]
          },
          {
            title: "i Notes Extention",
            description: "A real-time chat system for fast and responsive communication.",
            image: "/projects/project_inotes.png",
            live: "https://github.com/arjad/chrome-notes",
            github: "https://github.com/arjad/chrome-notes",
            technologies: ["HTML", "CSS", "React JS", "Webpack"]
          },
          {
            title: "Azoom Ecommers Website",
            description: "A real-time chat system for fast and responsive communication.",
            image: "/projects/project_azoom.png",
            live: "https://www.azoom.co.uk/",
            github: "https://github.com/arjad/azoom-ecomers",
            technologies: ["HTML", "CSS", "Bootstrap", "GitHub"]
          },
          {
            title: "Version Tracker Gem",
            description: "A real-time chat system for fast and responsive communication.",
            image: "/projects/project_version_tracker.png",
            live: "https://rubygems.org/gems/arjad_version_tracker/versions/0.5.0?locale=en",
            github: "https://github.com/arjad/arjad_version_tracker",
            technologies: ["Ruby", "Ruby on Rails"]
          },
          {
            title: "United Insurance Website",
            description: "Restaurant app to take order using website",
            image: "/projects/project_insurance.png",
            live: "https://mystifying-shaw-f4dc85.netlify.app/",
            github: "https://github.com/arjad/uic-new",
            technologies: ["React JS", "HTML", "SASS"]
          }, 
          {
            title: "WeHolding Real Estate  Website",
            description: "A real-time chat system for fast and responsive communication.",
            image: "/projects/project_weHolding.png",
            live: "https://weholdings.netlify.app/",
            github: "https://github.com/arjad/WeHoldings",
            technologies: ["Vue JS", "Mongo DB"]
          },
          {
            title: "NeoReach",
            description: "Website with animation and visual CSS",
            image: "/projects/project_neoreach.png",
            live: "https://affectionate-lovelace-1649f4.netlify.app/",
            github: "https://github.com/arjad/NeoReach",
            technologies: ["Animations", "HTML", "SASS"]
          },
          {
            title: "Food Menu App",
            description: "Restaurant app to take order using website",
            image: "/projects/project_freshmenu.png",
            live: "https://kaleidoscopic-cat-37f8fc.netlify.app/",
            github: "https://github.com/arjad/food-menu",
            technologies: ["Animations", "HTML", "SASS"]
          }, 
          
        ]
      };
    }
  }
</script>

<style scoped lang="scss">
.project-container {
  gap:20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  .card {
    width:30rem;
    transition: transform 0.3s ease-in-out;
    background: transparent;

    &:hover{
      transform: scale(1.02);
      z-index:2;
    }
    a:hover {
      text-decoration: underline;
    }
  }
}
</style>