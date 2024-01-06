<template>
  <section>
    <p id="skills" class="section__text__p1 text-center mt-5">Explore My</p>
    <h1 class="title text-center mb-5"> Practical Skills</h1>
    <div class="container">
      <div class="d-flex justify-content-center flex-wrap">
        <article
          class="position-relative"
          v-for="(skill, index) in skills"
          :key="index"
          data-aos="zoom-in" :data-aos-duration="getAosDuration(index)"
          @mouseover="toggleSkillLevel(index, true)"
          @mouseout="toggleSkillLevel(index, false)"
        >
          
          <h3>
            <i :class="[skill.iconClass, 'mr-2']"></i>
            {{ skill.name }}
          </h3>
          <p 
            class="skill-level badge badge-primary"
            v-if="skill.showLevel"
          >
            {{ skill.level }}
          </p>
        </article>
      </div>
     
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        { name: 'HTML', iconClass: 'fa-brands fa-html5', level: 'Experienced' ,showLevel: false  },
        { name: 'CSS', iconClass: 'fa-brands fa-css3-alt', level: 'Experienced' },
        { name: 'Bootstrap', iconClass: 'fa-brands fa-bootstrap', level: 'Intermediate' },
        { name: 'SASS', iconClass: 'fa-brands fa-sass', level: 'Experienced' },
        { name: 'JavaScript', iconClass: 'fa-brands fa-js', level: 'Intermediate' },
        { name: 'React', iconClass: 'fa-brands fa-react', level: 'Intermediate' },
        { name: 'Vue', iconClass: 'fa-brands fa-vuejs', level: 'Intermediate' },
        { name: 'Rails', iconClass: 'fa-solid fa-diamond', level: 'Intermediate' },
      ],
    };
  },
  methods: {
    toggleSkillLevel(index) {
      this.$set(this.skills, index, { ...this.skills[index], showLevel: !this.skills[index].showLevel });
    },
    getAosDuration(index) {
      return index * 400;
    },
  },
};
</script>

<style scoped>

article {
  width: 15rem;
  height: 5rem;
  gap: 0.5rem;

}
.skill-level {
  display: none;
}

article:hover .skill-level {
  display: block;
}

</style>