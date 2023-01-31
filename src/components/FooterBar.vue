<template>
  <v-footer class="bg-white text-center d-flex flex-column">
    <div>
      <v-btn href="https://www.linkedin.com/in/karol-zawisza/" color="primary" class="mx-4" icon="mdi-linkedin"
        variant="text" />
      <v-btn href="https://github.com/KarolZawisza555" color="primary" class="mx-4" icon="mdi-github" variant="text" />
    </div>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      'mdi-linkedin',
      'mdi-github',
    ],
  }),
}
</script>
