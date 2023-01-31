<template>
  <v-col cols="12" class="d-flex fill-height justify-center align-center">
    <v-card variant="tonal" class="ma-4 mt-10" max-width="1000">
      <template v-slot:title>
        <p class="text-h3 text-white font-weight-bold">
          Skills
        </p>
      </template>
      <template v-slot:text>
        <TransitionGroup name="list">
          <v-chip variant="elevated" v-for="item in usedLibrary" :key="item.name" class="ma-2" size="large"
            :color="item.color">
            {{ item.name }}
          </v-chip>
        </TransitionGroup>
      </template>
    </v-card>
  </v-col>
</template>

<script>
//
export default {
  data() {
    return {
      skills: [
        { name: 'Vue 3', color: "green" },
        { name: 'Vue 2', color: "green" },
        { name: 'Vuetify', color: "blue" },
        { name: 'Quasar', color: "blue" },
        { name: 'Pinia', color: "green" },
        { name: 'Vuex', color: "green" },
        { name: 'Bash', color: "black" },
        { name: 'Axios', color: "red" },
        { name: 'Vuevalidate', color: "green" },
        { name: 'Vscode', color: "blue" },
        { name: 'Git', color: "black" },
        { name: 'Node.js', color: "green" },
        { name: 'Python', color: "blue" },
        { name: 'Linux', color: "gray" }
      ],
      usedLibrary: [
        { name: 'Vue 3', color: "green" },
      ],
      listLibrary: [
        { name: 'Vue 2', color: "green" },
        { name: 'Vuetify', color: "blue" },
        { name: 'Vite', color: "blue" },
        { name: 'Nuxt 3', color: "green" },
        { name: 'Quasar', color: "blue" },
        { name: 'Pinia', color: "green" },
        { name: 'Vuex', color: "green" },
        { name: 'Bash', color: "black" },
        { name: 'Axios', color: "red" },
        { name: 'Vuevalidate', color: "green" },
        { name: 'Vscode', color: "blue" },
        { name: 'Git', color: "black" },
        { name: 'Node.js', color: "green" },
        { name: 'Python', color: "blue" },
        { name: 'Linux', color: "gray" }
      ],
    }
  },
  methods: {
    addItemToForList() {
      if (this.listLibrary.length) this.usedLibrary.push(this.listLibrary.pop())
    },
  },
  created() {
    this.interval = setInterval(() => this.addItemToForList(), 1000);
  },
};
</script>

<style>
.list-enter-active,
.list-leave-active {
  transition: all 0.4s cubic-bezier(0.075, 0.82, 0.165, 1);
}

.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(80px);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>

