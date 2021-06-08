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
      <section class="socials card fade-in delay-4">
        <span>Follow me : </span>
        <div>
          <a
            href="https://github.com/hvalette"
            target="_blank"
            rel="noopener noreferrer"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              version="1.1"
              width="60"
              height="60"
              viewBox="0 0 24 24"
            >
              <path
                fill="#000000"
                d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z"
              />
            </svg>
          </a>
          <a
            href="https://www.linkedin.com/in/hvalette"
            target="_blank"
            rel="noopener noreferrer"
          >
            <svg style="width: 60px; height: 60px" viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M19 3A2 2 0 0 1 21 5V19A2 2 0 0 1 19 21H5A2 2 0 0 1 3 19V5A2 2 0 0 1 5 3H19M18.5 18.5V13.2A3.26 3.26 0 0 0 15.24 9.94C14.39 9.94 13.4 10.46 12.92 11.24V10.13H10.13V18.5H12.92V13.57C12.92 12.8 13.54 12.17 14.31 12.17A1.4 1.4 0 0 1 15.71 13.57V18.5H18.5M6.88 8.56A1.68 1.68 0 0 0 8.56 6.88C8.56 5.95 7.81 5.19 6.88 5.19A1.69 1.69 0 0 0 5.19 6.88C5.19 7.81 5.95 8.56 6.88 8.56M8.27 18.5V10.13H5.5V18.5H8.27Z"
              />
            </svg>
          </a>
        </div>
      </section>
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
  padding: 2rem;
  display: grid;
  grid-template-rows: auto 1fr;
  span {
    font-size: 1.3rem;
    font-weight: bold;
  }
  div {
    display: flex;
    justify-content: space-around;
    align-items: center;
    a {
      svg {
        path {
          fill: var(--text-color);
        }
      }
    }
  }
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
    transform: translateZ(-50%);
    opacity: 0;
  }
  100% {
    transform: translateZ(0);
    opacity: 1;
  }
}
</style>
