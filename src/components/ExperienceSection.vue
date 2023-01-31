<template>
  <v-col cols="12" class="d-flex fill-height justify-center align-center">
    <v-card max-width="1000" class="ma-12">
      <template v-slot:title>
        <p class="text-h3 text-primary font-weight-bold">
          Experience
        </p>
      </template>
      <v-expansion-panels variant="popout" class="mt-2 mb-3 ">
        <WorkMako />
        <WorkFree />
        <WorkStrunobet />
        <WorkCerrad />
      </v-expansion-panels>
    </v-card>
  </v-col>
</template>

<script setup >
import WorkMako from "./WorkMako.vue"
import WorkStrunobet from "./WorkStrunobet.vue"
import WorkCerrad from "./WorkCerrad.vue"
import WorkFree from "./WorkFree.vue"
</script>
