<template>
  <main class="container">
    <div class="dashboard">
      <section class="angular card techno fade-in">
        <figure class="logo">
          <img src="~/assets/images/angular.svg" alt="angular logo" />
        </figure>
        <span>Angular</span>
      </section>
      <section class="tools card fade-in delay-8">
        <span>Some tools I like : </span>
        <div class="icons">
          <a
            href="https://code.visualstudio.com/"
            target="_blank"
            rel="noopener noreferrer"
            class="app-icon"
          >
            <img src="~/assets/images/vscode.svg" alt="vscode logo" />
          </a>
          <a
            href="https://www.jetbrains.com/fr-fr/webstorm/"
            target="_blank"
            rel="noopener noreferrer"
            class="app-icon"
          >
            <img src="~/assets/images/webstorm.svg" alt="webstorm logo" />
          </a>
          <a
            href="https://www.figma.com/"
            target="_blank"
            rel="noopener noreferrer"
            class="app-icon"
          >
            <img src="~/assets/images/figma.svg" alt="figma logo" />
          </a>
          <a
            href="https://www.netlify.com/"
            target="_blank"
            rel="noopener noreferrer"
            class="app-icon"
          >
            <img src="~/assets/images/netlify.svg" alt="netlify logo" />
          </a>
          <a
            href="https://fireship.io/"
            target="_blank"
            rel="noopener noreferrer"
            class="app-icon"
          >
            <img src="~/assets/images/fireship.png" alt="fireship logo" />
          </a>
        </div>
      </section>
      <section class="vuejs card techno fade-in delay-2">
        <figure class="logo">
          <img src="~/assets/images/vuejs.svg" alt="vuejs logo" />
        </figure>
        <span>VueJS</span>
      </section>
      <section class="jobs card fade-in delay-10"></section>
      <section class="theme card fade-in delay-9">
        <div class="buble" @click="toggleDarkMode">
          <span v-if="isDarkMode" class="mdi mdi-lightbulb-on"></span>
          <span v-else class="mdi mdi-lightbulb"></span>
        </div>
      </section>
      <section class="nestjs card techno fade-in delay-1">
        <figure class="logo">
          <img src="~/assets/images/nestjs.svg" alt="nestjs logo" />
        </figure>
        <span>NestJS</span>
      </section>
      <section class="firebase card techno fade-in delay-7">
        <figure class="logo">
          <img src="~/assets/images/firebase.svg" alt="firebase logo" />
        </figure>
        <span>Firebase</span>
      </section>
      <section class="socials card fade-in delay-4"></section>
      <section class="lang card fade-in delay-3"></section>
      <section class="lego card techno fade-in delay-6">
        <figure class="logo">
          <img src="~/assets/images/lego.png" alt="lego logo" />
        </figure>
      </section>
      <section class="resume card fade-in delay-5">
        <div class="header">
          <figure class="picture">
            <img
              src="https://avatars.githubusercontent.com/u/43471126?v=4"
              alt="my face"
            />
          </figure>
          <span class="name">Hi, I'm Henri Valette</span>
        </div>
        <div class="content">
          <p>
            I'm a {{ new Date().getFullYear() - 1996 }}yo french fullstack web
            developer
          </p>
          <p></p>
          <p>I received my master's degree in computer science in 2018</p>
          <p>Since then I am working at Atos in Lille</p>
        </div>
        <div class="made-with">
          <p>Made with ❤️ by me</p>
        </div>
      </section>
    </div>
  </main>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      isDarkMode: false,
    }
  },
  mounted() {
    this.isDarkMode = localStorage.getItem('dark') === 'true'
    if (this.isDarkMode) {
      document.body.classList.toggle('dark')
    }
  },
  methods: {
    toggleDarkMode() {
      document.body.classList.toggle('dark')
      this.isDarkMode = !this.isDarkMode
      localStorage.setItem('dark', `${this.isDarkMode}`)
    },
  },
})
</script>

<style lang="scss" scoped>
.container {
  width: 100vw;
  height: 100vh;
  margin: auto;
  display: grid;
  place-items: center;
  .dashboard {
    padding: 10px;
    width: 100vw;
    max-width: 1600px;
    height: 100vh;
    max-height: 1000px;
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    grid-template-rows: repeat(4, minmax(0, 1fr));
    gap: 10px;
    grid-template-areas:
      'angular tools vuejs jobs'
      'theme resume resume jobs'
      'nestjs resume resume firebase'
      'socials socials lang lego';
  }
}

.card {
  width: 100%;
  height: 100%;
  background: var(--background-accent);
  border-radius: 10px;
  overflow: hidden;
}

.logo {
  img {
    width: 100%;
    object-fit: contain;
  }
}
img {
  height: 100%;
}

.techno {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
  .logo {
    height: 50%;
  }
  span {
    font-size: 1.8rem;
    font-weight: bold;
  }
}

.angular {
  grid-area: angular;
}
.tools {
  grid-area: tools;
  padding: 2rem;
  span {
    font-size: 1.3rem;
    font-weight: bold;
  }
  .icons {
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
    grid-template-rows: repeat(auto-fit, minmax(60px, 1fr));
    gap: 1rem;
    padding: 1rem;
    .app-icon {
      padding: 0.6rem;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 2px 4px #00000022;
      border-radius: 10px;
      background: var(--background);
      filter: saturate(0.8);
      transition: 200ms;
      &:hover {
        filter: saturate(1.2);
      }
    }
  }
}
.vuejs {
  grid-area: vuejs;
}
.jobs {
  grid-area: jobs;
}
.theme {
  grid-area: theme;
  display: grid;
  place-items: center;
  .buble {
    cursor: pointer;
    font-size: 3rem;
  }
}
.resume {
  grid-area: resume;
  position: relative;
  .header {
    height: min(200px, 40%);
    background-color: #fbda61;
    background-image: linear-gradient(45deg, #edbb06 0%, #f100a8 100%);
    display: flex;
    align-items: center;
    padding: 1rem 2rem;
    .picture {
      height: 80%;
      img {
        border: 5px solid white;
        border-radius: 50%;
      }
    }
    .name {
      padding: 0 2rem;
      color: white;
      font-size: 1.8rem;
      font-weight: bold;
    }
  }
  .content {
    padding: 2rem;
    font-size: 1.2rem;
    line-height: 1.6;
    font-weight: 500;
  }
  .made-with {
    position: absolute;
    bottom: 0px;
    left: 50%;
    transform: translateX(-50%);
    padding: 1em;
  }
}
.nestjs {
  grid-area: nestjs;
}
.firebase {
  grid-area: firebase;
}
.socials {
  grid-area: socials;
}
.lang {
  grid-area: lang;
}
.lego {
  grid-area: lego;
}

.fade-in {
  opacity: 0;
  animation: 1000ms ease fade-in forwards;
}

.delay-1 {
  animation-delay: 100ms;
}
.delay-2 {
  animation-delay: 200ms;
}
.delay-3 {
  animation-delay: 300ms;
}
.delay-4 {
  animation-delay: 400ms;
}
.delay-5 {
  animation-delay: 500ms;
}
.delay-6 {
  animation-delay: 600ms;
}
.delay-7 {
  animation-delay: 700ms;
}
.delay-8 {
  animation-delay: 800ms;
}
.delay-9 {
  animation-delay: 900ms;
}
.delay-10 {
  animation-delay: 1000ms;
}

@media screen and (max-width: 768px) {
  .container {
    display: block;
    width: 100%;
    min-height: 100vh;
    .dashboard {
      padding: 0;
      display: block;
      width: 100%;
      height: 100%;
      section:not(.resume) {
        display: none;
      }
      .card {
        border-radius: 0;
      }
    }
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
