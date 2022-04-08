<template>
  <v-container class="pa-0">
    <v-row class=" ma-0">
      <v-col :cols="12" class="p-2">
        <h3 class="t1">Добро пожаловать в ИЖС Маркет!</h3>
      </v-col>
      <v-col :cols="6" class="pa-0">
        <div class="t-blocks bgc-1 ml-2 mr-1 my-0 p-0">
          <div class="m-2 t-text">Выберите проект дома, а разные
            застройщики предложат цены
          </div>
        </div>
      </v-col>
      <v-col :cols="6" class="pa-0">
        <div class="t-blocks bgc-2 ml-1 mr-2 my-0 p-0">
          <div class="m-2 t-text">Выберите проект дома, а разные
            застройщики предложат цены
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row class="ma-0 main-block mt-5 pd-0">
      <v-col :cols="12">
        <v-sheet
    class="mx-auto"
    elevation="8"
    max-width="800"
  >
    <v-slide-group
      v-model="model"
      class="pa-4"
      prev-icon="mdi-minus"
      next-icon="mdi-plus"
      show-arrows
    >
      <v-slide-item
        v-for="n in 15"
        :key="n"
        v-slot="{ active, toggle }"
      >
        <v-card
          :color="active ? 'primary' : 'grey lighten-1'"
          class="ma-4"
          height="200"
          width="100"
          @click="toggle"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <v-scale-transition>
              <v-icon
                v-if="active"
                color="white"
                size="48"
                v-text="'mdi-close-circle-outline'"
              ></v-icon>
            </v-scale-transition>
          </v-row>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'HomePage',
  setup(){
    let model = null
    let elementList = ref([{
      name: '',
      active: false
    },{
      name: '',
      active: false
    },])
    let active = ref(null)
    return {model,active,elementList}
  },
  data: () => ({
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader',
      },
      {
        text: 'github',
        href: 'https://github.com/vuetifyjs/vuetify',
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/vuetifyjs/awesome-vuetify',
      },
    ],
    importantLinks: [
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com',
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify',
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs',
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify',
      },
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com',
      },
      {
        text: 'Roadmap',
        href: 'https://vuetifyjs.com/introduction/roadmap/',
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
}
</script>

<style>
/*@import url("src/assets/fonts/mont/stylesheet.css");*/

@font-face {
  font-family: 'Mont';
  src: url('~@/assets/fonts/mont/Mont-SemiBold.eot');
  src: local('Mont SemiBold'), local('Mont-SemiBold'),
  url('~@/assets/fonts/mont/Mont-SemiBold.eot?#iefix') format('embedded-opentype'),
  url('~@/assets/fonts/mont/Mont-SemiBold.woff2') format('woff2'),
  url('~@/assets/fonts/mont/Mont-SemiBold.woff') format('woff'),
  url('~@/assets/fonts/mont/Mont-SemiBold.ttf') format('truetype');
  font-weight: 600;
  font-style: normal;
}

.t1 {
  font-family: 'Mont', serif;
  font-style: normal;
  font-weight: 800;
  font-size: 24px;
  line-height: 31px;

  color: #FFFFFF;
}

.t-blocks {
  background: linear-gradient(135.55deg, #A7A6CB -5.43%, #8989BA 107.62%);
  border-radius: 10px;
}

.bgc-1 {
  background: linear-gradient(135.55deg, #A7A6CB -5.43%, #8989BA 107.62%);
}

.bgc-2 {
  background: linear-gradient(134.43deg, #C79081 26.26%, #DFA579 105.21%);
}

.custom {
  z-index: 3;
  position: absolute;
  width: 30%;
  height: 50%;
  left: 112px;
  top: 8px;

  background: linear-gradient(135.3deg, #8989BA 7.36%, #A7A6CB 101.97%);
  filter: blur(8px);
}

.t-text {
  font-family: 'Mont', serif;
  font-style: normal;
  font-weight: 600;
}

.main-block {
  background-color: white;
  border-radius: 15px 15px 0 0;
}
</style>
