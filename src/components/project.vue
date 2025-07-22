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
              <i class="fa-solid fa-arrow-up-right-from-square"></i> Live Demo
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
    data() {
      return {
        projects: [
          {
            title: "TravelLodge",
            description: "A full-stack hotel booking app with user authentication, geo-based search, and Mapbox integration.",
            image: "https://media.istockphoto.com/id/1497396873/photo/ready-for-starting-my-beach-holiday.jpg?s=612x612&w=0&k=20&c=Rfb7IbYAZR1hNTF6KUDYq8CVu9Yr4wRgK2VLZIZyORY=",
            live: "https://travellodge-5emi.onrender.com/",
            github: "https://github.com/roshansahu61/TravelLodge",
            technologies: ["React", "Node.js", "MongoDB", "Passport.js", "Mapbox"]
          },
          {
            title: "NexChat",
            description: "A real-time chat app with group and private messaging using WebSockets and authentication.",
            image: "https://blog.zegocloud.com/wp-content/uploads/2024/03/signal-chat-app.jpg",
            live: "https://chat-szrq.onrender.com/",
            github: "https://github.com/roshansahu61/Nexchat",
            technologies: ["React", "Node.js", "MongoDB", "Socket.io"]
          },
          {
            title: "Job Portal",
            description: "Job posting and application system with recruiter/applicant dashboards and secure login.",
            image: "https://media.licdn.com/dms/image/v2/D5612AQHmWpsKqCEUgQ/article-cover_image-shrink_600_2000/article-cover_image-shrink_600_2000/0/1692110377639?e=2147483647&v=beta&t=8o8pbq1bZtrQjOZxyCis8GkK8FtHx38WqMoea3qjPB0",
            live: "https://job-portal-v7kw.vercel.app/",
            github: "https://github.com/roshansahu61/Job-Portal",
            technologies: ["React", "Node.js", "MongoDB", "Express"]
          },
          {
            title: "Akhand Bharat",
            description: "A patriotic single-page site showcasing Indian unity, tradition, and heritage with responsive UI.",
            image: "https://images.moneycontrol.com/static-mcnews/2024/08/20240814035536_Daily-Horoscope-13.png?impolicy=website&width=770&height=431",
            live: "https://akhand-bharat-1.vercel.app/",
            github: "https://github.com/roshansahu61/akhand-bharat",
            technologies: ["React", "Tailwind CSS"]
          }
        ]
      };
    }
  }
</script>

<style scoped lang="scss">
.project-container {
  gap: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;

  .card {
    width: 30rem;
    transition: transform 0.3s ease-in-out;
    background: transparent;

    &:hover {
      transform: scale(1.02);
      z-index: 2;
    }

    a:hover {
      text-decoration: underline;
    }
  }
}
</style>
