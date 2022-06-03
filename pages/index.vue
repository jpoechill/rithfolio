<template>
  <div>


    <div class="container pt-md-4">
      <div class="row pt-0 mt-3 mb-5">
        <div class="offset-md-1 col-md-3 pb-5 p-md-0">
          <div class=" px-5 px-md-0">
            <img src="/IMG_1565.jpg" class="w-100 border" style="border-radius: 500px;" alt="">
          </div>
        </div>
        <div class="offset-md-1 col-md-6 px-5 p-md-0">
          <p class="">
            Greetings! <br><br> I'm Po, and I specialize in building web applications with Vue.js. <br>
          </p>
          <p>
            I have a background in art/design, and have a passion making digital experiences look, feel and work great.
            Along with technology, I also enjoy strange things like crossfit, training capoeira, and space-exploration video games. 🦾 🧘‍♂️ 🤓 <br><br> 
            If you are interested in learning more about me, or my work, please feel free to get in touch!
            <br>
            <!-- <span class="text-muted">
              <small><em>
                Hashtags: #Algorithms, #Design, #Javascript, #Vue.js, #HTML/CSS, #Git
              </em></small>
            </span> -->
          </p>
          <p class="text-right pt-2">
            <a href="mailto: heys@rithfolio.com">Email</a>, <a href="https://github.com/jpoechill" target="new">Github</a>, <a href="https://linkedin.com/in/porith" target="new">LinkedIn</a>
          </p>
          <!-- <p style="color: #777;">
            <em>
              Keywords: Design, Prototyping, Javascript, Vue.js, HTML/CSS, Git
            </em>
          </p> -->

        </div>
        <!-- <div class="col-md-12 pt-5 mt-3">
          <hr>
        </div> -->
      </div>
    </div>

    <div class="border-top custom-bg" style="background-color: #fdfdfd;">
    <div class="container pt-4 mt-3 pb-5">
      <div class="row pt-0 my-1 pb-0">
        <div class="col-md-12 text-center">
          <h5 class="pb-0 mb-0 text-muted">
            Recent Projects
          </h5>
        </div>
      </div>

      <div class="row mt-0 pb-5">
        <div class="col-md-6 h-100" v-for="(project, index) in projects" :key="index">
          <div class="px-4 mt-5 mb-2">
            <div class="bg-white pb-1 box-shadow" style="border-radius: 10px; overflow: hidden; border: 1px solid #ddd;">
              <div class="w-100">
                <div class="w-100 overflow-hidden">
                  <a :href="project.url" target="new">
                    <img :src="project.img" class="w-100 zoom" alt="">
                  </a>
                </div>
                <div class="pt-4 pb-2 px-5">
                  <span class="font-weight-bold font-size-lg text-light mb-3 d-block">
                    <h4>
                      {{ project.title }}
                    </h4>  
                  </span>
                  <p class="mb-4 text-muted">
                    {{ project.description }}
                  </p>
                  <p class="mt-3 pb-0 text-right">
                    <span v-for="(link, index) in project.links" :key="index">
                      <a :href="link.url">{{ link.title }}</a>
                      <span v-if="index !== project.links.length - 1"> | </span>
                    </span>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
    
    </div>

    <div class="border-top">
      <div class="container" style="opacity: 1!important;">
        <div class="row py-5">
          <div class="col-md-12 pb-5 px-5 text-center text-dark pt-5">
            <!-- <hr class="pt-5 pb-1 my-5"> -->
            "I fear not the man who has practiced 10,000 kicks once, but I fear the man who has practiced one kick 10,000 times."
            <br>
            – Bruce Lee
          </div>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: 'Product Feedback App',
          description: 'A frontend, product feedback application that accounts for adding, commenting and updating feature requests for products and teams.',
          img: '/browser-12.png',
          url: 'https://compassionate-hugle-3311b0.netlify.app/',
          links: [
            {
              title: 'Github',
              url: 'https://github.com/jpoechill/product-feedback-fem'
            },
            {
              title: 'Demo',
              url: 'https://compassionate-hugle-3311b0.netlify.app/'
            }
          ]
        },
        {
          title: 'Invoice App',
          description: 'A frontend, invoice application for creating, updating and tracking invoices for entreprenuers and freelancers.',
          img: '/browser-13.jpg',
          url: 'https://sweet-muffin-869709.netlify.app/',
          links: [
            {
              title: 'Github',
              url: 'https://github.com/jpoechill/invoice-app'
            },
            {
              title: 'Demo',
              url: 'https://sweet-muffin-869709.netlify.app/'
            }
          ]
        },
        {
          title: 'Multi Page Marketing Website',
          description: 'PPCS Restore is a national, family-run, commercial building restoration company based in the Bay Area.',
          img: '/browser-09.jpg',
          url: 'https://ppc-restore.com/',
          links: [
            {
              title: 'Github',
              url: 'https://github.com/jpoechill/ppcs'
            },
            {
              title: 'Live Site',
              url: 'https://ppc-restore.com/'
            }
          ]
        },
        {
          title: 'Squarespace Marketing Website',
          description: 'Mellana Café is a cafe located in North Oakland, offering juices, sandwiches, and specialty coffee.',
          img: '/browser-11.jpg',
          url: 'https://mellanacafe.com',
          links: [
            {
              title: 'Live Site',
              url: 'https://mellanacafe.com'
            }
          ]
        },
      ]
    }
  },
  created() {
    // this.$router.push({
    //     path: '/working'
    // })
  },
  transition: 'fade'
}
</script>

<style scoped>
.text-light {
  color: #333 !important;
}

.zoom {
  transition: transform .5s ease;
}

.zoom:hover {
  cursor: pointer;
  transform: scale(1.04); /* (150% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
}

.fixed-ratio {
  width: 100%;
  padding-bottom: 63.78%;
}

.box-shadow {
  -webkit-box-shadow: 5px 6px 14px 2px rgba(0,0,0,0.25); 
  box-shadow: 5px 6px 14px 2px rgba(0,0,0,0.1);
}

.custom-bg {
  background-color: #b7b7b70f;
  background-image: linear-gradient(135deg, #ffffff 25%, transparent 25%), linear-gradient(225deg, #ffffff 25%, transparent 25%), linear-gradient(45deg, #ffffff 25%, transparent 25%), linear-gradient(315deg, #ffffff 25%, rgb(183 183 183 / 0%) 25%);
  background-position:  40px 0, 40px 0, 0 0, 0 0;
  background-size: 80px 80px;
  background-repeat: repeat;
}

</style>
