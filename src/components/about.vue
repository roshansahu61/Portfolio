<template>
  <section id="about" class="container">
    <Heading :title="'About Me'" :subtitle="'Want to know me'" />

    <div class="position-relative">
      <div class="verticle-line position-absolute"></div>
      <div data-aos="fade-left" data-aos-duration="1000" class="mt-4 ml-5">
        <h2 class='mb-4'> <i class="fa-solid fa-briefcase"></i> Experience</h2>
        <div class='w-100 text-green'>
          <h4 class='d-inline'> Front-End Web Developer Intern - Sept 2023 to Oct 2023 </h4>
        </div>
        <h6> <a class='text-blue' href='https://codeclause.com/'> CodeClause, Bangalore, India </a></h6>
        <ul>
          <li> Built responsive front-end components with HTML, CSS, and JavaScript, reducing load times by 150ms. </li>
          <li> Optimized web interfaces through debugging and performance improvements for seamless functionality. </li>
        </ul>
        <div class="skills mb-5">
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">HTML5</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">CSS3</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">JavaScript</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">ReactJS</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">Tailwind CSS</span>
        </div>

        <h4 class='text-green'> Software Developer Instructor - Present </h4>
        <h6> <a class='text-blue'href= 'https://www.ccbp.in/'>NxtWave,Hyderabad,Telangana</a> </h6>
        <ul>
          <li> Created visually appealing, user-friendly interfaces, using CSS grid and flexbox layouts for responsive design. </li>
          <li> Utilized react components & npm modules to develop modular, reusable UI elements for efficient front-end development. </li>
        </ul>
        <div class="skills mb-5">
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">HTML</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">CSS</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">SCSS</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">JavaScript</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">Bootstrap</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">Tailwind CSS</span>
          <span class="badge rounded-pill px-3 py-2 mx-2 border border-dark">React JS</span>
        </div>
      </div>
    </div>

    <div class="position-relative mt-5">
      <div class="verticle-line position-absolute"></div>

      <div data-aos="fade-left" data-aos-duration="1000" class="mt-4 ml-5">
        <h2 class='mb-4'><i class="fa-solid fa-user-graduate"></i> Education </h2>
        
        <h4 class='text-green'> B.E. in Information Science and Engineering - 2021–2025 </h4>
        <h6><a class='text-blue' href='https://nitte.edu.in/'> NITTE Meenakshi Institute of Technology, Karnataka, India. </a></h6>
        <p> CGPA: 7.93/10 — Developed strong foundation in software engineering, data structures, OOP, DBMS, and full-stack development. </p>

        <h4 class='text-green'> Class XII - 2019–2020 </h4>
        <h6>Oxford Public School, Jharkhand, India</h6>
        <p> Percentage: 78.6% </p>

        <h4 class='text-green'> Class X - 2017–2018 </h4>
        <h6>Vivekananda Vidya Mandir, Jharkhand, India</h6>
        <p> Percentage: 84% </p>
      </div>
    </div>
  </section>
</template>

<script>
import Heading from "./common/heading.vue";
export default {
  components: {
    Heading,
  },
  data() {
    return {
      activeSection: 'experience',
      startDate: "2022-07-01"
    };
  },
  computed: {
    calculatedExperience() {
      const startDate = new Date(this.startDate);
      const currentDate = new Date();
      const yearsDifference = currentDate.getFullYear() - startDate.getFullYear();
      const isFullYear = currentDate.getMonth() >= startDate.getMonth() && currentDate.getDate() >= startDate.getDate();

      return isFullYear ? yearsDifference : yearsDifference - 1;
    },
  },
  methods: {
    setActiveSection(section) {
      this.activeSection = section;
    },
  },
};
</script>

<style scoped>
.about-containers {
  gap: 2rem;
}
.details-container {
  padding: 1.5rem;
  flex: 1;
  width: 15vw;
  border-radius: 2rem;
  border: rgb(53, 53, 53) 0.1rem solid;
  border-color: rgb(163, 163, 163);
  text-align: center;
}
.details-container:hover {
  cursor: pointer;
  background: lightgrey;
}

ul {
  line-height: 30px;
  font-size: 1.2rem;
}

.verticle-line{
  width: 15px;
  height: 100%;
  background: linear-gradient(to right, #47BA87 50%, #34495E 50%);
}
.verticle-line-right{
  right:0;
}

.text-green{
  color: #47BA87;
}
.text-blue{
  color: #34495E;
  text-decoration: underline;
}

@media screen and (max-width: 375px) {
  .details-container h3 {
    font-size: 14px;
  }
}
</style>
