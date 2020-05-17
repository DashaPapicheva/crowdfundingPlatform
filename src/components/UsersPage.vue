<template>
  <div class="Users">
    <div class="header">
      <h1>Наши участники</h1>
    </div>
    <v-container fluid>
      <v-row dense> 
        <v-col
          v-for="user in users"
          :key="user.id"
        >
          <user-card :user="user"/>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import UserCard from "./UserPage/UserCard";
import axios from 'axios';

export default {
  name: "UsersPage",
  components: {
    UserCard,
  },
  data: () => ({
    users: [],
  }),
  created() {
    this.getUsers()
  },
  methods: {
    getUsers() {
      axios.get('data/users.json')
      .then((response) => {this.users = response.data.users})
    },
  },
}
</script>

<style scoped>
.header {
  margin-left: 1rem;
}
.Users {
  margin-top: 4em;
}
</style>