<template>
  <div id="skills">
    <h1>Skills</h1>
    <h4>FRONT-END & DESIGN</h4>
    <div class="skill-card-grid">
      <div class="skill-card" v-for="skill in skills" :key="skill">
        <img :src="getImgUrl(skill.pic)" :alt="skill.pic" />
        {{ skill.title }}
      </div>
    </div>
    <h4>BACK-END & DATABASE</h4>
    <div class="skill-card-grid">
      <div class="skill-card" v-for="beskill in beskills" :key="beskill">
        <img :src="getImgUrl(beskill.pic)" :alt="beskill.pic" />
        {{ beskill.title }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      skills: [
        { pic: "html5.svg", title: "HTML" },
        { pic: "css3-alt.svg", title: "CSS" },
        { pic: "node-js.svg", title: "NodeJS" },
        { pic: "vuejs.svg", title: "VueJS" },
        { pic: "figma.svg", title: "Figma" }
      ],
      beskills: [
        { pic: "json.svg", title: "JSON" },
        { pic: "strapi.svg", title: "Strapi" },
        { pic: "postqresql.svg", title: "PostgreSQL" },
        { pic: "knexjs.png", title: "KnexJS" }
      ]
    };
  },
  methods: {
    getImgUrl(pic) {
      return require("../assets/svg/" + pic);
    }
  }
};
</script>

<style scoped>
h1 {
  font-size: 4rem;
  text-align: center;
  margin: 0 auto;
  width: 50%;
  margin-bottom: 1rem;
}

h4 {
  font-family: "Poppins", sans-serif;
  font-weight: 300;
  text-align: center;
  margin: auto;
  width: 60%;
  height: 125px;
  font-size: 1.5rem;
  margin-top: 1rem;
  margin-bottom: -5rem;
  padding-top: 0.5rem;
  background: rgb(249, 247, 249);
  background: linear-gradient(
    0deg,
    rgba(249, 247, 249, 1) 12%,
    rgba(181, 213, 222, 1) 32%,
    rgba(109, 177, 193, 0.8) 78%,
    rgba(109, 177, 193, 0.8) 100%
  );
}

.skill-card-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.skill-card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 175px;
  height: 175px;
  border-radius: 50%;
  background: rgb(249, 247, 249);
  background: linear-gradient(
    0deg,
    rgba(249, 247, 249, 1) 12%,
    rgba(181, 213, 222, 1) 32%,
    rgba(109, 177, 193, 1) 78%,
    rgba(109, 177, 193, 1) 100%
  );
  margin: 1rem;
  padding: 1rem;
  font-family: "Poppins", sans-serif;
  text-align: center;
  box-shadow: 1px 2px 1px rgba(109, 177, 193, 0.5);
}

.skill-card img {
  width: 75px;
  opacity: 0.95;
}

#skills h4:nth-of-type(2) {
  margin-top: 2rem;
}

@media (max-width: 495px) {
  h4 {
    width: 90%;
  }
}
</style>
