<template>
  <div>
    <footer class="mt-5 text-lg-start" id="contact">
      <hr class="my-4" />
      <section class="row">
        <div class="col-md-3 col-lg-3 col-xl-3 mx-auto mt-3">
          <h6 class="text-uppercase mb-4 font-weight-bold">Contact Details</h6>
          <p v-if="contact.linkedin">
            <a :href="contact.linkedin" target="_blank">
              <i class="fab fa-linkedin"></i> LinkedIn
            </a>
          </p>
          <p v-if="contact.github">
            <a :href="contact.github" target="_blank">
              <i class="fab fa-github"></i> GitHub
            </a>
          </p>
          <p v-if="contact.email">
            <a :href="`mailto:${contact.email}`">
              <i class="fas fa-envelope"></i> {{ contact.email }}
            </a>
          </p>
          <p v-if="contact.phone">
            <i class="fas fa-phone"></i> {{ contact.phone }}
          </p>
          <p v-if="contact.resume">
            <a :href="contact.resume" target="_blank">
              <i class="fas fa-file-download"></i> View Resume
            </a>
          </p>
          <p>
            <i class="fas fa-map-marker-alt"></i> Jharkhand, India
          </p>
        </div>

        <div class="col-md-2 col-lg-2 col-xl-2 mx-auto mt-3">
          <h6 class="text-uppercase mb-4 font-weight-bold">Services</h6>
          <p>Website Development</p>
          <p>App Development</p>
          <p>Others</p>
        </div>

        <div class="col-md-4 col-lg-3 col-xl-3 mx-auto mt-3">
          <h6 class="text-uppercase mb-4 font-weight-bold">Links</h6>
          <p class="scroll-to" @click="scrollToSection('summary')">Summary</p>
          <p class="scroll-to" @click="scrollToSection('about')">About</p>
          <p class="scroll-to" @click="scrollToSection('practicle_skills')">Skills</p>
          <p class="scroll-to" @click="scrollToSection('projects')">Projects</p>
        </div>

        <div class="col-md-3 col-lg-2 col-xl-2 mx-auto mt-3">
          <h6 class="text-uppercase mb-4 font-weight-bold">Follow us</h6>
          <a v-if="contact.linkedin" class="btn btn-floating m-1" :href="contact.linkedin" role="button">
            <i class="fab fa-linkedin-in"></i>
          </a>
          <a v-if="contact.github" class="btn btn-floating m-1" :href="contact.github" role="button">
            <i class="fab fa-github"></i>
          </a>
          <a class="btn btn-floating m-1" href="https://medium.com/@your_username" role="button">
            <i class="fa-solid fa-m"></i>
          </a>
          <a class="btn btn-floating m-1" href="https://leetcode.com/your_username" role="button">
            <i class="fa-brands fa-dev"></i>
          </a>
          <a class="btn btn-floating m-1" href="https://discordapp.com/users/your_username" role="button">
            <i class="fa-brands fa-discord"></i>
          </a>
        </div>
      </section>
      <hr />
      <div class="text-center p-3">
        © 2025 Made with
        <a :href="contact.github || '#'">Vue.js</a>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "FooterComponent",
  data() {
    return {
      contact: {
        linkedin: "https://www.linkedin.com/in/roshan-sahu-467104246",
        github: "https://github.com/roshansahu61",
        email: "roshansahu5700@gmail.com",
        phone: "6360846624",
        resume: "https://drive.google.com/file/d/11knC03R8QvA0lhRx_K652DLLx6bETRWa/view?usp=sharing",
      },
    };
  },
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: "smooth" });
      }
    },
  },
};
</script>

<style scoped>
.scroll-to {
  cursor: pointer;
}
footer {
  section.row p a {
    color: black;
  }
}
</style>
