<template>
  <v-app-bar app color="white" class="mb-10">
    <v-avatar class="ma-4" size="x-large">
      <v-img cover src="../assets/ZawiszaKarol5.png" alt="Karol" />
    </v-avatar>
    <p class="text-primary font-weight-bold">

      Zawisza Karol
    </p>
    <v-spacer></v-spacer>
    <div class="d-none d-sm-flex">
      <v-btn text color="primary" @click="scroll('skills')">skills</v-btn>
      <v-btn text color="primary" @click="scroll('projects')">Projects</v-btn>
      <v-btn text color="primary" @click="scroll('experience')">experience</v-btn>
    </div>
    <ContactDialog />
  </v-app-bar>
</template>

<script>
import ContactDialog from './ContactDialog.vue';

export default {
  components: { ContactDialog },
  data() {
    return {
      showDialog: false
    }
  },
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
    activeDialog() {
      this.showDialog = true
    },
  },
};
</script>
