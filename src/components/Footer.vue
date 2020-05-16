<template>
  <v-footer
    padless
  >
    <v-card
      tile
      color="orange"
      class="mainFooter"
    >

      <v-card-text class="footerText white--text">
        <div class="aboutUs">
          <h1 class="footerHead">О нас</h1>
          <ul>
            <li><a href="#">Кто мы?</a></li>
            <li><a href="#">Как работает Крауд</a></li>
            <li><a href="#">Партнёры</a></li>
          </ul>
        </div> 
        <div class="contacts"> 
          <h1 class="footerHead">Контакты</h1>
          <ul>
            <li>Почта: privet@mail.ru</li>
            <li>Телефон: +6 666 666 66 66</li>
          </ul>
        </div>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="lastWord white--text">
        {{ new Date().getFullYear() }} — <strong>Крауд</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
}
</script>

<style scoped>

  .mainFooter {
    width: 100%;
    display: flex;
    flex-direction: column;;
  }
  .footerText {
    width: 100%;
    line-height: 1.5rem;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }

  .footerHead {
    margin-bottom: 1rem;
  }

  .aboutUs ul, .contacts ul {
    padding-left: 0;
    margin-left: 0;
  }

  .aboutUs ul li, .contacts ul li {
    list-style-type: none;
    padding-left: 0;
    margin-left: 0;
    text-decoration: none;
  }

    .aboutUs ul li a {
    color: white;
    text-decoration: none;
  }

  .lastWord {
    text-align: center;
  }
</style>