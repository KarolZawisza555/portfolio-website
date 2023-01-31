<template>
  <v-col cols="12" id="projects" class="d-flex fill-height justify-center align-center">
    <div style="max-width:1000px">
      <p class="text-h3 mb-5 mt-3  text-white font-weight-bold">
        Projects
      </p>
      <v-row>
        <template v-for="project in projects" :key="project.index">
          <v-col :lg="4" :md="6" :sm="6" :xs="12">
            <ProjectCard v-bind="project" />
          </v-col>
        </template>
      </v-row>
    </div>
  </v-col>
</template>

<script>
import ProjectCard from './ProjectCard.vue';
//
export default {
  components: { ProjectCard },
  data() {
    return {
      projects:
        [
          { title: 'Portfolio website', description: "Current page", subtitleinfo: "Presentation skills", projectGithubName: "registration-forms", libraries: ['vue 3', "vuetify"], image: "1" },
          { title: 'Validate example', description: "Validation on vuevalidate and more", subtitleinfo: "Validation forms", projectGithubName: "registration-forms", libraries: ['vue3', "quasar", "vueuse", "vuevalidate"], image: "../assets/image1.png" },
          { title: 'Animal compare', description: "Quasar fun", subtitleinfo: "Compare animals by quasar", projectGithubName: "quasar-animal-compare", libraries: ['vue3', "quasar", "axios"], image: "../assets/image1.png" },
          { title: 'Pinia & Apex Charts', description: "Extended version of TODO lists with points and totaling charts", subtitleinfo: "Charts APEX", projectGithubName: "security", libraries: ['vue3', "quasar", "vueuse", "vuevalidate"], image: "../assets/image1.png" },
          { title: 'Django Website', description: "Learn Django3", subtitleinfo: "Interesting page with the CSS basics", projectGithubName: "My-old-website-django", libraries: ['python', "sql", "HTML5", "CSS"], image: "../assets/image1.png" },
        ]
    }
  },
};
</script>

