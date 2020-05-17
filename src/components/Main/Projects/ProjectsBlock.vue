<template>
  <div class="Projects">
    <v-row>
      <v-col>
        <h1 class="projHeader">
          Проекты
        </h1>

        <v-card class="mx-auto wholeCard" max-width="800">
          <div class="flexSection">
            <v-card-title class="flexItem"
              >Cнежкометатели для всех</v-card-title
            >

            <v-card-text class="flexItem">
              <p>
                Для всех любителей поиграть в снежки — <br /><span class="gun"
                  >Тройной снежкометатель</span
                >.
              </p>
            </v-card-text>

            <v-card-subtitle class="authorCard flexItem">
              <v-img
                src="https://femmie.ru/wp-content/uploads/2019/09/stefan-teresiak-eKOfPcY1bU4-unsplash-696x457.jpg"
                class="authorImg"
              >
              </v-img>
              <p>Автор проекта: <br />Ирина Денисова</p>
            </v-card-subtitle>

            <v-card-actions class="flexItem">
              <v-btn color="orange" text>
                Поделиться
              </v-btn>

              <v-btn color="orange" text>
                Подробнее>>
              </v-btn>
            </v-card-actions>
          </div>

          <div class="flexSection">
            <v-img
              class="mainProjImage flexItem"
              height="200"
              width="400"
              src="https://www.zarubejom.ru/wp-content/uploads/2019/12/18090626.388862.7332.jpg"
            >
              <p class="status">Самый популярный</p>
            </v-img>

            <div class="flexItem">
              <v-progress-linear height="15" width="12" :value="aim" stream>
                <strong>{{ Math.ceil(aim) }}%</strong>
              </v-progress-linear>
            </div>
          </div>
        </v-card>

        <h2 class="projHeader">
          Могут заинтересовать
        </h2>
      </v-col>
    </v-row>
    <v-container fluid>
      <v-row dense>
        <v-col v-for="project in projects" :key="project.id">
          <project-card :project="project" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import ProjectCard from "./ProjectCard";
import axios from "axios";

export default {
  name: "ProjectsBlock",
  components: {
    ProjectCard,
  },
  data: () => ({
    aim: 83,
    projects: [],
  }),
  methods: {
    getProjects() {
      axios.get("data/projects.json").then((response) => {
        this.projects = response.data.items;
      });
    },
  },
  created() {
    this.getProjects();
  },
};
</script>

<style scoped>
.projHeader {
  padding-left: 1rem;
  text-align: left;
}

.wholeCard {
  column-count: 2;
}

.flexItem {
  page-break-inside: avoid;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.mainProjImage {
  margin-left: auto;
  margin-right: 0;
  display: flex;
  justify-content: flex-end;
  align-items: flex-start;
}

.gun {
  font-weight: bold;
}

.authorImg {
  border-radius: 50%;
  max-width: 7rem;
  margin-left: 16px;
  margin-right: 26px;
  margin-bottom: 16px;
}

.v-card__subtitle {
  padding: 0;
}

.v-responsive__content {
  vertical-align: top;
}

.status {
  color: white;
  font-size: 2rem;
  font-weight: bold;
  text-align: right;
  margin-right: 10px;
}

.v-progress-linear {
  width: 100%;
  margin-top: 2rem;
  margin-bottom: 1rem;
}
</style>
