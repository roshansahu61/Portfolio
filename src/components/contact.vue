<template>
<<<<<<< Updated upstream
  <footer id="contact" class="footer d-flex justify-content-center alig-item-center">
    <Heading :title="'Contact Me'" :subtitle="'Want To Get in Touch'" />
    <img class='footer-me' src="../assets/me-footer.png" alt="profile pic" />
=======
    <footer class="text-center mt-5 text-lg-start text-white" id="contact">
        <section class="row">
            <div class="col-md-3 col-lg-3 col-xl-3 mx-auto mt-3">
              <h6 class="text-uppercase mb-4 font-weight-bold">Contact Details</h6>
              <p>
                <a class="text-white" href="https://www.linkedin.com/in/arjad/" target="_blank">
                  <i class="fab fa-linkedin"></i> LinkedIn
                </a>
              </p>
              <p>
                <a class="text-white" href="https://github.com/arjad" target="_blank">
                  <i class="fab fa-github"></i> GitHub
                </a>
              </p>
              <p>
                <a class="text-white" href="mailto:arjadgohar14@gmail.com">
                  <i class="fas fa-envelope"></i> arjadgohar14@gmail.com
                </a>
              </p>
              <p>
                <i class="fas fa-map-marker-alt"></i> Chauburji Park, Lahore, Pakistan
              </p>
            </div>
>>>>>>> Stashed changes

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
              <a class="btn btn-primary btn-floating m-1" style="background-color: #3b5998" href="#" role="button">
                <i class="fab fa-facebook-f"></i>
              </a>
              <a class="btn btn-primary btn-floating m-1" style="background-color: #55acee" href="#" role="button">
                <i class="fab fa-twitter"></i>
              </a>
              <a class="btn btn-primary btn-floating m-1" style="background-color: #dd4b39" href="#" role="button">
                <i class="fab fa-google"></i>
              </a>
              <a class="btn btn-primary btn-floating m-1" style="background-color: #ac2bac" href="#" role="button">
                <i class="fab fa-instagram"></i>
              </a>
              <a class="btn btn-primary btn-floating m-1" style="background-color: #0082ca" href="#" role="button">
                <i class="fab fa-linkedin-in"></i>
              </a>
              <a class="btn btn-primary btn-floating m-1" style="background-color: #333333" href="#" role="button">
                <i class="fab fa-github"></i>
              </a>
            </div>
        </section>
      <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2)">
        © 2025 Made with 
        <a class="text-white" href="https://github.com/arjad/Portfolio">Vue.js</a>
      </div>
    </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  methods: {
     scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
};
</script>

<<<<<<< Updated upstream
<style lang="scss" scoped>
.footer {
  position: relative;
  width: 100%;
  background: #47BA87;
  flex-direction: column;
  margin-top: 25vh;
  color: white;
}
.footer-me{
  height:100%;
  width:45rem;
  opacity:0.1;
  position: absolute;
  right: 0px;
}

.social-icon__item{
  list-style: none;
  padding-top: 15px;
  font-size: 14px;
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
.cursor{
=======
<style scoped>
.scroll-to {
>>>>>>> Stashed changes
  cursor: pointer;
}
</style>
