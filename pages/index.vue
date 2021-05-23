<template>
  <main class="container">
    <div class="dashboard">
      <section class="angular card techno">
        <figure class="logo">
          <img src="~/assets/images/angular.svg" alt="angular logo" />
        </figure>
        <span>Angular</span>
      </section>
      <section class="tools card">
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
      <section class="vuejs card techno">
        <figure class="logo">
          <img src="~/assets/images/vuejs.svg" alt="vuejs logo" />
        </figure>
        <span>VueJS</span>
      </section>
      <section class="jobs card"></section>
      <section class="theme card">
        <div class="buble" @click="toggleDarkMode">
          <span v-if="isDarkMode" class="mdi mdi-lightbulb-on"></span>
          <span v-else class="mdi mdi-lightbulb"></span>
        </div>
      </section>
      <section class="nestjs card techno">
        <figure class="logo">
          <img src="~/assets/images/nestjs.svg" alt="nestjs logo" />
        </figure>
        <span>NestJS</span>
      </section>
      <section class="firebase card techno">
        <figure class="logo">
          <img src="~/assets/images/firebase.svg" alt="firebase logo" />
        </figure>
        <span>Firebase</span>
      </section>
      <section class="socials card"></section>
      <section class="lang card"></section>
      <section class="lego card techno">
        <figure class="logo">
          <img src="~/assets/images/lego.png" alt="lego logo" />
        </figure>
      </section>
      <section class="resume card">
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
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    gap: 10px;
    .app-icon {
      flex: 0 0 60px;
      height: min(50%, 60px);
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
    line-height: 2;
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
</style>
