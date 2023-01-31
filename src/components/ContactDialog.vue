<template>
  <v-btn text variant="outlined" class="mr-2" color="primary" @click="dialog = true">Contact</v-btn>
  <div class="text-center">
    <v-dialog v-model="dialog" max-width="600px">
      <v-card>
        <v-card-text class="text-center">
          <p class="ma-3">
            <v-icon color="primary" size="large" icon="mdi-phone"></v-icon>
            570-096-077
          </p>
          <p class="ma-3">
            <v-icon color="primary" size="large" icon="mdi-email"></v-icon>
            inz.zawisza.karol@gmail.com
          </p>
          <v-btn href="https://www.linkedin.com/in/karol-zawisza/" color="primary" class="mx-4" icon="mdi-linkedin"
            variant="text" />
          <v-btn href="https://github.com/KarolZawisza555" color="primary" class="mx-4" icon="mdi-github"
            variant="text" />
        </v-card-text>
        <v-card-actions>
          <v-btn color="primary" block @click="dialog = false">Close</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
export default {
  name: 'ContactDialog',
  data: () => {
    return {
      dialog: false,
    }
  },
}
</script>
