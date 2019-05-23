<template>
  <div>
    <div class="row pt-2">
      <div class="col-md-6" v-for="(project, index) in projects" :key="index">
        <span class="weight-600">{{ project.title }}</span>
        <p class="mb-1">
          {{ project.description }}
        </p>
        <span class="bg-dark font-small text-light p-1 pl-2 pr-2">Visit Project</span>
        <br>
        <br>
      </div>
    </div>
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
          url: 'https://project.netlify.com',
        },
        {
          title: 'Lead Genius FE Exercise',
          description: 'A frontend exercise for Lead Genuis – building out a simple to-do list application, from start to finish.',
          url: 'https://project.netlify.com',
        },
        {
          title: 'Eaze FE Exercise',
          description: 'A frontend exercise for Eaze – building a simple GIPHY API viewer in the style of Netflix.',
          url: 'https://project.netlify.com',
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


.z-index-back {
  z-index: -1000;
}
</style>
