<template>
  <section class="section container" id="about">
    <h2 class="section__title"></h2>
    <div class="about__container">
      <div class="about__text">
        <p>👋 Hello, I’m Roshan — a passionate full-stack web developer based in India. I specialize in crafting dynamic and responsive websites using the MERN stack (MongoDB, Express, React, Node.js) and Angular.</p>
        <p>💻 I’ve built full-stack projects like a chat app, job portal, and e-commerce platform. I'm skilled in third-party APIs, authentication systems, and WebSockets.</p>
        <p>🚀 I enjoy transforming ideas into scalable software and continuously learning new technologies. I'm effective in both solo and team settings.</p>
        <p>📫 Let’s connect and create something amazing together!</p>
      </div>
      <div class="about__image">
        <img src="@/assets/images/about.png" alt="About Image" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped lang="scss">
.about__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 5rem;
  padding: 2rem 0;

  @media (max-width: 768px) {
    flex-direction: column;
    text-align: center;
  }
}

.about__text {
  flex: 1;
  font-size: 1.6rem;
  line-height: 1.5;
  font-weight: 700;
  color: #4f5362;

  p {
    margin-bottom: 2rem;
    text-align: justify;
  }
}

.about__image img {
  flex: 1;
  width: 100%;
  max-width: 400px;
  border-radius: 10rem;
}
</style>
