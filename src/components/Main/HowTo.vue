<template>
  <v-card>
    <v-card-title>
      <h1 class="headerHowTo">Как это работает</h1>
    </v-card-title>
    <v-col class="howToObjects">
      <ol>
        <li>Создание проекта</li>
        <li>Ожидание средств от добровольцев</li>
        <li>Запуск проекта</li>
      </ol>
      <iframe width="560" height="315" src="https://www.youtube.com/embed/S0KLbRna40o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </v-col>
  </v-card>
</template>

<script>
export default {
  name: "HowTo",
  data: () => ({

  })
}
</script>

<style scoped>
  .headerHowTo {
    font-size: 2rem;
  }
  
  .howToObjects {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .howToObjects ol  {
    margin-left: 2rem;
    line-height: 3rem;
  }

  .howToObjects iframe  {
    margin-left: 5rem;
    max-width: 50%;
  }

</style>