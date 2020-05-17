<template>
  <div>
    <v-hover v-slot:default="{ hover }">
      <v-card
      height="200px"
      width="200px"
      >
        <v-img
          :src="user.photo"
          class="white--text align-end"
          gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
          height="200px"
          width="200px"
        >
          <v-card-title 
            class="subtitle-1"
            v-text="user.name" 
            v-show="hover == false"
          />
          <v-expand-transition>
            <div
              v-if="hover"
              class="transition-fast-in-fast-out orange darken-2 v-card--reveal white--text"
              style="height: 100%;"
            >
              <p>Имя: {{ user.name }}</p>
              <p>Должность: {{ user.rank }}</p>
              <p>Возраст: {{ user.age }}</p>
              <p>Регион: {{ user.city }}</p>
            </div>
          </v-expand-transition>
        </v-img>
      </v-card>
    </v-hover>
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

<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  /* justify-content: center; */
  opacity: .7;
  position: absolute;
  width: 100%;
  overflow: auto;
}
</style>
