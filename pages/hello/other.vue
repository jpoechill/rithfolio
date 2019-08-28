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
          <br>
          <br>
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
          title: 'Shipt FE Exerise',
          description: 'A frontend exercise for Shipt – building out a production-ready application from design mock and requirements brief.',
          github: 'https://github.com/jpoechill/vueshiptexercise',
          url: 'https://focused-wilson-aa0b5a.netlify.com/'
        },
        {
          title: 'Lead Genius FE Exercise',
          description: 'A frontend exercise for Lead Genuis – building out a simple to-do list application, from start to finish.',
          github: 'https://github.com/jpoechill/vueleadgeniusdemo',
          url: 'https://serene-fermi-baa469.netlify.com'
          
        },
        {
          title: 'Eaze FE Exercise',
          description: 'A frontend exercise for Eaze – building a simple GIPHY API viewer in the style of Netflix.',
          github: 'https://github.com/jpoechill/vueeazeexercise',
        }
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

.mh-special {
  min-height: 440px;
}

.logo {
  min-width: 150px;
}

.link-white {
  color: #FFF;
}

.link-white:hover {
  text-decoration: none;
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
  font-weight: 600;
  color:#333;
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
