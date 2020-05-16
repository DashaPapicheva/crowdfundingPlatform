<template>
  <v-container>

    <div class="mainImg">
      <div class="onPictureWithBnt">
      <div class="onPicture ">
        <h1 class="name">Краудфандинговая площадка</h1>
        <p>Здесь готовы поддержать деньгами понравившийся проект</p>

        <ul>
          <li>Бизнес</li>
          <li>Творчество</li>
          <li>Технологии</li>
          <li>Социальные проекты</li>
          <li>И многое-многое другое</li>
        </ul>
      </div>

        <v-btn
        href
        target="_blank"
        text
        max-width="200"
        class="BNTclass"
      >
        <span class="mr-2">Создать проект</span>
      </v-btn>

      </div>
    </div>

    <v-row class="text-center">


      <v-col>
        <h1 class="projHeader">
          Проекты
        </h1>


      <h2 class="projHeader">Могут заинтересовать</h2>


        <v-row justify="center">
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-row>

      </v-col>


    </v-row>
    <HowTo/>
    <Partners/>
  </v-container>
</template>

<script>
import Partners from './Main/Partners';
import HowTo from './Main/HowTo';

  export default {
    name: 'HelloWorld',
    components: {
      Partners,
      HowTo
    },
    data: () => ({
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/layout/pre-defined',
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>

<style scoped>
  .container {
    padding: 0;
    max-width: 100%;
  }

  .projHeader {
    padding-left: 1rem;
    text-align: left;
  }

  .mainImg {
    background-image: url(../assets/crowdfounding.jpg) ;
    width: 100%;
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 70vh;
  }

  .onPictureWithBnt {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
  }

  .onPicture {
    padding-top: 4rem;
    padding-left: 3%;
    vertical-align: middle;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    align-content: center;
    }

    .BNTclass {
      border-radius: 10rem;
      width: 15rem;
      background-color: orange;
      text-align: center;
      margin-left: 2rem;
    }

  .name {
    color: black;
    font-size: 2rem;
  }

</style>