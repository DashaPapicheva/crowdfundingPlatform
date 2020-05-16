<template>
  <div class="Users">
    <div class="header">
      <h1>Наши участники</h1>
    </div>
    <v-container fluid>
      <v-row dense> 
        <v-col
          v-for="user in users"
          :key="user.name"
          :cols="user.flex"
        >
          <user-card :user="user"/>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import UserCard from "./UserPage/UserCard";

export default {
  name: "UsersPage",
  components: {
    UserCard,
  },
  data: () => ({
    users: [
      {
        name: "Joe",
        photo: "https://bloximages.chicago2.vip.townnews.com/nwitimes.com/content/tncms/assets/v3/editorial/0/d9/0d98cbc7-0408-518e-a67d-50ba01ca1bfa/5a7e4016d73b4.image.jpg",
        age: "23",
        city: "moscow",
        rank: "shitbuster",
        flex: 3,
      },
      {
        name: "Emily",
        photo: "https://bodyimagemovement.com/shop/wp-content/uploads/2019/10/scarf-2f-.jpg",
        age: "235",
        city: "Muhosransk",
        rank: "whaa",
        flex: 3,
      },
      {
        name: "Joe",
        photo: "https://bloximages.chicago2.vip.townnews.com/nwitimes.com/content/tncms/assets/v3/editorial/0/d9/0d98cbc7-0408-518e-a67d-50ba01ca1bfa/5a7e4016d73b4.image.jpg",
        age: "23",
        city: "moscow",
        rank: "shitbuster",
        flex: 3,
      },
      {
        name: "Emily",
        photo: "https://bodyimagemovement.com/shop/wp-content/uploads/2019/10/scarf-2f-.jpg",
        age: "235",
        city: "Muhosransk",
        rank: "whaa",
        flex: 3,
      },
      {
        name: "Joe",
        photo: "https://bloximages.chicago2.vip.townnews.com/nwitimes.com/content/tncms/assets/v3/editorial/0/d9/0d98cbc7-0408-518e-a67d-50ba01ca1bfa/5a7e4016d73b4.image.jpg",
        age: "23",
        city: "moscow",
        rank: "shitbuster",
        flex: 3,
      },
      {
        name: "Emily",
        photo: "https://bodyimagemovement.com/shop/wp-content/uploads/2019/10/scarf-2f-.jpg",
        age: "235",
        city: "Muhosransk",
        rank: "whaa",
        flex: 3,
      },
    ]
  }),
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