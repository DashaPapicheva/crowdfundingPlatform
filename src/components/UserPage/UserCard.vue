<template>
  <div>
    <v-card>
      <v-img
        :src="user.photo"
        class="white--text align-end"
        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
        height="200px"
      >
        <v-card-title v-text="user.name"></v-card-title>
      </v-img>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "UserCard",
  props: {
    user: {
            type: Object,
            default: null
        },
  }
}
</script>
