<template>
  <div>
    <transition name="fade" appear>
      <div class="row pt-2">
        <div class="col-md-6" v-for="(project, index) in projects" :key="index">
          <span class="weight-600">{{ project.title }}</span>
          <p class="mb-1">
            {{ project.description }}
          </p>
          <span v-if="project.url" class="bg-dark font-small text-light p-1 pl-2 pr-2">
            <a :href="project.url" target="_blank" class="link-white">Visit Project</a>
          </span>
          <span v-if="project.github" class="bg-dark font-small text-light p-1 pl-2 pr-2">
            <a :href="project.github" target="_blank" class="link-white">View Github</a>
          </span>
          <br><br>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {
      emailText: "Email",
      projects: [
        {
          title: ' Destiny 2 Data Exporter',
          description: 'A tool for Destiny 2 (PS4) players that allows the ability to export games stats in .JSON format.',
          url: 'https://xcrucibleexporter.netlify.com/',
          github: 'https://github.com/jpoechill/xcrucibleexporter'
        },
        {
          title: 'Infamous – Destiny 2 Gambit Tracker',
          description: 'A tool for Destiny 2 (PS4) players to track and view their Gambit W/L records, and related stats.',
          url: 'http://xinfamous.tk/',
          github: 'https://github.com/jpoechill/xinfamous'
        },
        {
          title: 'xNews – Aggregate News API Viewer',
          description: 'A personal, aggregate news viewer that allow one to select their own news sources, and add custom links from around the web.',
          url: 'https://xnews.netlify.com',
          github: 'https://github.com/jpoechill/vuefrontendrtalk_demo'
        },
        {
          title: 'Vue, Stripe Payments',
          description: 'An application utilizing Vue.js, Firebase Cloud Function, and Stripe API to demonstrate the ability to make custom payments without a proper backend.',
          url: 'https://zen-johnson-ca4f83.netlify.com/',
          github: 'https://github.com/jpoechill/vuepayme'
        },
        {
          title: 'Simple Pinterest Clone',
          description: 'A Pinterest clone, experimenting with Firebase database features, with attention to micro-animations.',
          url: 'https://wizardly-stallman-dd6025.netlify.com/',
          github: 'https://github.com/jpoechill/vue-pinterestclone'
        },
        {
          title: 'Monastium – Accomodations For Monasteries',
          description: 'A prototypal web application for finding accommodations and other goods from world monasteries.',
          url: 'https://monastium.com/',
          // github: 'https://project.netlify.com'
        },
      ]
    }
  },
  methods: {
    handleToggle () {
      this.emailText = 'heys@rithfolio.com'
    }
  },
}
</script>

<style scoped>
body, html {
  font-size: 18px;
  height: 100%;
}

.link-white {
  color: #FFF;
}

.link-white:hover {
  text-decoration: none;
}

.mh-special {
  min-height: 440px;
}

.logo {
  min-width: 150px;
}

.portrait {
  min-height: 500px;
}

.special {
  font-size: 22px;
}

.font-small {
  font-size: 14px;
}

.weight-400 {
  font-weight: 400;
}

.weight-600 {
  font-weight: 600;
}

.bg-dark:hover {
  background-color: #555!important;
}

.z-index-back {
  z-index: -1000;
}
</style>
