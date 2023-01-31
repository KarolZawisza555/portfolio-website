<template>
  <v-card class="pa-3 ma-3" max-width="500">
    <!-- <v-img height="200px" cover src="{{ image }}" /> -->
    <v-card-title>
      {{ title }}
    </v-card-title>
    <v-card-subtitle>
      {{ subtitleinfo }}
    </v-card-subtitle>
    <v-card-actions>
      <v-btn :href="myGithub + projectGithubName" color="" variant="text">
        Github
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
    </v-card-actions>
    <div class="px-4">
      <v-chip v-for="item in libraries" :key="item.index" class="ma-1">{{ item }}</v-chip>
    </div>
    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>
        <v-card-text>
          {{ description }}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>
<script>
export default {
  props: {
    title: String,
    subtitleinfo: String,
    image: String,
    description: String,
    projectGithubName: String,
    libraries: Array
  },
  data: () => ({
    show: false,
    myGithub: "https://github.com/KarolZawisza555/"
  }),
  method: {
    getImgUrl(pet) {
      return require('../assets/' + pet)
    }
  }
}
</script>
