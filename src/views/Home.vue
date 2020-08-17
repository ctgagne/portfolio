<template>
  <div class="home">
    <div class="hero">
      <h2>Welcome!<br />My name is Charles Gagne, but you can call me Chaz</h2>
      <h1>Freelance UX/UI Designer and Developer</h1>
      <h5>
        I’m a junior web developer from South Carolina, now living in Leipzig,
        DE.
      </h5>
      <div class="home-buttons">
        <a class="btn" href="#portfolio">Portfolio</a>
        <a class="btn" href="#skills">Skills</a>
      </div>
    </div>
    <div class="world-map">
      <img src="@/assets/worldmap2.png" />
    </div>
    <div id="portfolio">
      <Portfolio />
    </div>
    <div id="skills">
      <Skills />
    </div>
    <div id="contact">
      <Contact />
    </div>
  </div>
</template>

<script>
import Portfolio from "@/components/Portfolio.vue";
import Skills from "@/components/Skills.vue";
import Contact from "@/components/Contact.vue";
export default {
  name: "Home",
  components: {
    Portfolio,
    Skills,
    Contact
  }
};
</script>

<style scoped>
.home {
  color: var(--dark-text);
  padding: 2rem;
  padding-top: 10rem;
  margin: 0 auto;
  max-width: 1400px;
  text-align: left;
}

.hero {
  display: flex;
  flex-direction: column;
  margin: 0 4rem;
  justify-content: center;
}

.world-map {
  position: relative;
  display: flex;
  margin: 0 auto;
  margin-top: -1rem;
  justify-content: center;
}

.world-map img {
  width: 95%;
}

.btn {
  display: inline-block;
  cursor: pointer;
  border: none;
  width: 125px;
  text-align: center;
  font-weight: 400;
  border-radius: 0.2rem;
  padding: 0.5rem 1rem;
  font-size: 1.5rem;
  margin: 1rem;
  color: var(--light-text);
  background-color: var(--dark-background);
  font-family: "Yesteryear", cursive;
}

.btn:hover {
  color: var(--component-color);
}

.home-buttons :first-child {
  margin-left: 0;
}

h1 {
  font-size: 5rem;
  font-weight: 700;
}

h2,
h3,
h5 {
  font-family: "Poppins", sans-serif;
  font-weight: 600;
}

h4 {
  text-align: center;
  top: 60%;
  background-color: rgba(109, 177, 193, 0.6);
  padding: 0.5rem 1rem;
  border-radius: 1rem;
  font-weight: 400;
  font-family: "Yesteryear", cursive, sans-serif;
  font-size: 2rem;
}

#portfolio {
  padding: 3rem;
  margin: 0 auto;
  background: rgb(249, 247, 249);
  background: linear-gradient(
    90deg,
    rgba(249, 247, 249, 0) 0%,
    rgba(249, 247, 249, 0.7) 11%,
    rgba(109, 177, 193, 0.7) 32%,
    rgba(109, 177, 193, 0.7) 66%,
    rgba(249, 247, 249, 0.7) 91%,
    rgba(249, 247, 249, 0) 100%
  );
}

#skills {
  padding: 3rem;
}

#contact {
  padding: 3rem;
  margin: 0 auto;
  background: rgb(249, 247, 249);
  background: linear-gradient(
    90deg,
    rgba(249, 247, 249, 0) 0%,
    rgba(249, 247, 249, 0.7) 11%,
    rgba(109, 177, 193, 0.7) 32%,
    rgba(109, 177, 193, 0.7) 66%,
    rgba(249, 247, 249, 0.7) 91%,
    rgba(249, 247, 249, 0) 100%
  );
}
</style>
