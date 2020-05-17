<template>
  <div class="partners">
    <v-card tile>
      <v-card-title>
        <h1 class="partnersHeader">Партнёры</h1>
      </v-card-title>

      <v-carousel hide-delimiters height="300">
        <v-carousel-item v-for="(item, i) in partners" :key="i">
          <v-img :src="item.logo" class="items" />
        </v-carousel-item>
      </v-carousel>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "Partners",
  data: () => ({
    partners: [
      {
        name: "mars",
        logo:
          "https://www.mars.com/sites/g/files/jydpyr316/files/Mars%20Wordmark%20RGB%20Blue.png",
      },
      {
        name: "kitekat",
        logo:
          "https://i.pinimg.com/originals/d0/2f/e5/d02fe53cad8f75f0eade7b3fdbe7bf74.jpg",
      },
      {
        name: "sberbank",
        logo: "https://allvectorlogo.com/img/2016/11/sberbank-logo.png",
      },
    ],
  }),
};
</script>

<style scoped>
.partners {
  padding-bottom: 12rem;
}
.partnersHeader {
  font-size: 2rem;
}
.items {
  max-width: 40rem;
  max-height: 20rem;
  margin: auto;
}
</style>
