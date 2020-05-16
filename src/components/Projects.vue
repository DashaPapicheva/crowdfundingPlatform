<template>
  <div>
    <v-card>
      <v-img
        :src="project.photo"
        class="white--text align-end"
        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
        height="200px"
      >
        <v-card-title v-text="project.name"></v-card-title>
      </v-img>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    user: {
            type: Object,
            default: null
        },
  }
}
</script>