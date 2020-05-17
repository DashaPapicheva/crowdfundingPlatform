<template>
  <div>
  <v-card
    class="mx-auto card"
    max-width="400"
  >
    <v-img
      :src="project.picture"
      height="200px"
    ></v-img>

    <v-card-title   
    v-text="project.name"
    >
    </v-card-title>

    <div class="progress">
   <v-progress-linear
     height="15"
     width="12"
     v-model="project.funded"
     stream
   >
     <strong>{{ Math.ceil(project.funded) }}%</strong>
   </v-progress-linear>
   </div>

    </v-card>

  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    project: {
            type: Object,
            default: null
        },
  }
}
</script>

<style scoped>
  .card, .progress {
    margin: 1rem;
  }

</style>