<template>
  <div id="app">
    <header>
      <div id="nav">
        <div class="navigation-logo">
          <a href="/">CG</a>
        </div>
        <ul class="navigation-menu-desktop">
          <li>
            <a href="#portfolio">Portfolio</a>
          </li>
          <li>
            <a href="#skills">Skills</a>
          </li>
          <li>
            <a href="#contact">Contact</a>
          </li>
        </ul>
      </div>
    </header>
    <router-view />
    <footer>
      © 2020 Charles Gagne
    </footer>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Monoton&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;900&family=Yesteryear&display=swap");
#app {
  font-family: "Yesteryear", cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

:root {
  --light-text: #f9f7f9;
  --dark-text: #221e29;
  --light-background: #f9f7f9;
  --dark-background: #221e29;
  --primary-color: #168ccc;
  --component-color: #6db1c1;
  --accent-dark: #666362;
}

* {
  padding: 0;
  margin: 0;
  outline: none;
  box-shadow: none;
  box-sizing: border-box;
}

body {
  font-size: 1.25rem;
  line-height: 1.4;
  background-color: var(--light-background);
  color: var(--dark-text);
}

html {
  scroll-behavior: smooth;
}

a,
a:visited {
  text-decoration: none;
  font-weight: bold;
  color: var(--dark-text);
  padding: 0.5rem 1rem;
  border-radius: 0.2rem;
}
a:hover {
  text-decoration: underline;
  background-color: rgba(189, 189, 189, 0.3);
}

header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.1);
  background-color: rgba(240, 239, 241, 0.3);
  z-index: 999;
  background-image: url("~@/assets/topography.svg");
}

#nav {
  max-width: 1400px;
  min-height: 75px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
  padding: 0.5rem 2rem;
}

li {
  list-style-type: none;
  font-size: 1.5rem;
}

.navigation-menu-desktop li:nth-child(3) a {
  border: 1px solid var(--primary-color);
  text-decoration: none;
}

.navigation-menu-desktop li {
  display: inline;
}

.navigation-menu-desktop li:not(:first-child) {
  margin-left: 2rem;
}

.navigation-logo {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: left;
}

.navigation-logo :first-child,
.navigation-logo a:hover {
  font-family: "Monoton", cursive;
  font-size: 2.5rem;
  text-decoration: none;
  font-weight: 400;
  text-align: left;
  background-color: none;
}

footer {
  bottom: 0;
  left: 0;
  right: 0;
  box-shadow: 0px -1px -1px rgba(0, 0, 0, 0.1);
  background-color: rgba(240, 239, 241, 0.3);
  z-index: 999;
  font-family: "Poppins", sans-serif;
  font-size: 1rem;
}

@media (max-width: 550px) {
  #nav {
    justify-content: center;
    padding-bottom: 1rem;
    background-color: rgba(240, 239, 241, 0.7);
  }
}
</style>
