<template>
  <div id="portfolio-main">
    <h1>Portfolio</h1>
    <h5>Check Out My Recent Work</h5>
    <div class="card-grid">
      <div
        id="card"
        class="curryon"
        @mouseover="curryonhover = true"
        @mouseleave="curryonhover = false"
      >
        <img src="@/assets/curryon2.png" /><img src="@/assets/curryon1.png" />
        <transition name="appear">
          <div class="curryon-flipped" v-if="curryonhover">
            <div class="site-code">
              <a href="https://loving-feynman-16214a.netlify.app/">Site</a>
              <a href="https://github.com/chrisfrie/curry-on">Code</a>
            </div>
          </div>
        </transition>
      </div>

      <h3>Curry On! Food Challenge App</h3>
      <div
        id="card"
        class="ergo"
        @mouseover="hover = true"
        @mouseleave="hover = false"
      >
        <div class="screen-shot"></div>
        <transition name="appear">
          <div class="ergo-flipped" v-if="hover">
            <div class="site-code">
              <a href="https://ergo-lazar.netlify.app">Site</a>
              <a href="https://github.com/ctgagne/ergo-lazar">Code</a>
            </div>
          </div>
        </transition>
      </div>
      <h3>Praxis fur Ergotherapie - Sophie Lazar</h3>

      <div
        id="card"
        class="obj"
        @mouseover="objhover = true"
        @mouseleave="objhover = false"
      >
        <div class="screen-shot"></div>
        <transition name="appear">
          <div class="ergo-flipped" v-if="objhover">
            <div class="site-code">
              <a href="https://objectivelysubjectivepodcast.com">Site</a>
              <a href="https://github.com/ctgagne/objectively-subjective"
                >Code</a
              >
            </div>
          </div>
        </transition>
      </div>
      <h3>The Objectively Subjective Podcast</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "Portfolio",
  data() {
    return {
      hover: false,
      objhover: false,
      curryonhover: false
    };
  }
};
</script>

<style scoped>
.card-grid {
  max-width: 60rem;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
#card {
  display: flex;
  border-radius: 1rem;
  margin: 2rem;
  margin-top: 3rem;
}

.curryon {
  position: relative;
  display: flex;
  justify-content: center;
  align-content: center;
  overflow: visible;
}

.obj {
  display: flex;
  width: 533px;
  height: 300px;
  background-image: url("~@/assets/objectivelyss2.png");
  background-size: 100%;
  background-repeat: no-repeat;
  background-attachment: absolute;
  background-position: center;
  -webkit-box-shadow: 7px 7px 7px 0px rgba(0, 0, 0, 0.25);
  -moz-box-shadow: 7px 7px 7px 0px rgba(0, 0, 0, 0.25);
  box-shadow: 7px 7px 7px 0px rgba(0, 0, 0, 0.25);
}

.ergo {
  display: flex;
  justify-content: center;
  align-content: center;
  width: 533px;
  height: 300px;
  overflow: hidden;
  background-image: url("~@/assets/ergo-lazar.png");
  background-size: 100%;
  background-repeat: no-repeat;
  background-attachment: absolute;
  background-position: center;
  -webkit-box-shadow: 7px 7px 7px 0px rgba(0, 0, 0, 0.25);
  -moz-box-shadow: 7px 7px 7px 0px rgba(0, 0, 0, 0.25);
  box-shadow: 7px 7px 7px 0px rgba(0, 0, 0, 0.25);
}

.ergo-flipped {
  display: flex;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.2);
  justify-content: center;
  align-items: center;
  font-size: 1.8rem;
}

.ergo-flipped a {
  width: 5ch;
  height: 3ch;
  background-color: rgba(255, 255, 255, 0.8);
  color: var(--dark-text);
  padding: 0.5rem 1rem;
  border-radius: 1rem;
}

.curryon-flipped {
  position: absolute;
  top: 25%;
  left: 25%;
  display: flex;
  width: 50%;
  height: 50%;
  background-color: rgba(0, 0, 0, 0.2);
  justify-content: center;
  align-items: center;
  font-size: 1.8rem;
  border-radius: 1rem;
}

.curryon-flipped a {
  width: 5ch;
  height: 4ch;
  background-color: rgba(255, 255, 255, 0.7);
  color: var(--dark-text);
  padding: 0.5rem 1rem;
  border-radius: 1rem;
  box-shadow: 7px 7px 5px 0px rgba(0, 0, 0, 0.25);
}

.curryon-flipped .site-code :first-child {
  margin-right: 1.2rem;
  margin-left: -3rem;
}

.ergo-flipped :first-child {
  margin-right: 1rem;
}

.curryon img {
  height: 90%;
  border: 1px solid rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 7px 7px 5px 0px rgba(0, 0, 0, 0.25);
  -moz-box-shadow: 7px 7px 5px 0px rgba(0, 0, 0, 0.25);
  box-shadow: 7px 7px 5px 0px rgba(0, 0, 0, 0.25);
}

.curryon :first-child {
  margin-right: -3rem;
}

.curryon :nth-child(2) {
  margin-top: 2rem;
}

h1 {
  font-size: 4rem;
  text-align: center;
  margin: 0 auto;
  width: 50%;
  padding-bottom: -1rem;
}

h5 {
  padding: -1rem;
  text-align: center;
  font-weight: 200;
  font-size: 1.25rem;
  padding-bottom: 2rem;
  font-family: "Poppins", sans-serif;
}

h3 {
  padding: 1rem;
  font-family: "Poppins";
  font-weight: 400;
  margin-top: -2rem;
  border: 1px solid rgba(22, 140, 204, 0.2);
  background-color: rgba(22, 140, 204, 0.1);
  border-bottom-left-radius: 1rem;
  border-bottom-right-radius: 1rem;
}

h3:first-of-type {
  padding-top: 4rem;
  margin-top: -5rem;
}

.appear-enter-active,
.appear-leave-active {
  transition: opacity 0.7s;
}
.appear-enter, .appear-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

@media (max-width: 550px) {
  #card {
    margin: 0.5rem;
    margin-top: 1rem;
  }
  .ergo {
    width: calc(350px - 16px);
    height: 188px;
    padding: 0;
    margin: 0;
  }
  .obj {
    width: calc(350px - 16px);
    height: 188px;
    padding: 0;
    margin: 0;
  }
  .curryon {
    width: 188px;
    height: calc(350px - 16px);
    padding: 0;
    margin: 0;
  }
  h3 {
    padding: 1rem;
    font-family: "Poppins";
    font-weight: 400;
    margin-top: -0.7rem;
    font-size: 1rem;
    border: 1px solid rgba(22, 140, 204, 0.2);
    background-color: rgba(22, 140, 204, 0.1);
    border-bottom-left-radius: 1rem;
    border-bottom-right-radius: 1rem;
  }

  h3:first-of-type {
    padding-top: 22rem;
    margin-top: -22rem;
  }
}
</style>
