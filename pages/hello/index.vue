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
          title: 'PPCS – Restoration Services',
          description: 'PPCS is a building restoration company based in the SF, Bay Area. They are a national, family run company, having been in business for over 35 years.',
          url: 'https://project.netlify.com',
        },
        {
          title: 'PortraitsDaily.com',
          description: 'PortraitsDaily.com is a personal, art portfolio website, displaying portraits of people done in watercolors, and pen-and-ink.',
          url: 'https://project.netlify.com',
        },
        {
          title: 'Poyear.com – Specialty Cupcakes and Macaroons',
          description: 'Poyear is an entrepenuer, and baker from Oakland, CA. She work through her home, and takes orders for cakes, cupcakes, and macaroons.',
          url: 'https://project.netlify.com',
        },
        {
          title: 'Code Self Study – Community Group',
          description: 'Code Self Study is community programming group located the Berkeley, East Bay Area. Members come from all walks of life, ',
          url: 'https://project.netlify.com',
        },
        {
          title: 'BWL Delivery – Oakland Beverages Store',
          description: 'BWL Delivery is a specialty beverages store in Oakland, CA. They are a family run business, and have been in operation for over 30 years.',
          url: 'https://project.netlify.com',
        },
        {
          title: 'PerfectCanvas.art',
          description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officia sequi odit adipisci, voluptatum eligendi est eveniet possimus vitae unde numquam?',
          url: 'https://project.netlify.com',
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
