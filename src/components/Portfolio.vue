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
              <a href="https://objectivelysubjectivepodcast.com">Site</a>
              <a href="#">Code</a>
            </div>
          </div>
        </transition>
      </div>

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
              <a href="#">Code</a>
            </div>
          </div>
        </transition>
      </div>

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
              <a href="#">Code</a>
            </div>
          </div>
        </transition>
      </div>
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
  display: grid;
  grid-gap: 25px;
  grid-template-columns: 450px 515px;
  grid-template-rows: 290px 290px;
}
#card {
  display: flex;
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  border-radius: 1rem;
}

.curryon {
  position: relative;
  display: flex;
  justify-content: center;
  align-content: center;
  grid-column: 1;
  grid-row: 1 / span 2;
  place-content: center;
  overflow: visible;
  margin-left: -16px;
}

.obj {
  display: flex;
  justify-content: center;
  align-content: center;
  grid-column: 2;
  overflow: hidden;
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
  grid-column: 2;
  grid-row: 1;
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
  margin-top: 3rem;
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
  font-weight: 300;
  font-size: 1.5rem;
  padding-bottom: 2rem;
  font-family: "", sans-serif;
}

.appear-enter-active,
.appear-leave-active {
  transition: opacity 0.7s;
}
.appear-enter, .appear-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
