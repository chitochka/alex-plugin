<template>
  <v-app app>
    <!-- <MyMenu></MyMenu> -->
    <!-- <v-app-bar app></v-app-bar> -->

    <v-main>
      <v-container>
        <!-- <SlovnikSeznam> </SlovnikSeznam> -->
        <!-- Hello World <div> aa : {{danie}}</div> -->

        <v-card>
          <v-tabs  v-model="tab"  background-color="deep-purple accent-4"  centered  dark  icons-and-text>
            <v-tabs-slider></v-tabs-slider>
            <v-tab href="#tab-1">    Slovnik    <v-icon>mdi-flag-variant-outline</v-icon>  </v-tab>
            <v-tab href="#tab-2">    KZT - CZK    <v-icon>mdi-currency-kzt</v-icon>  </v-tab>
            <v-tab href="#tab-3">    Slider    <v-icon>mdi-arrow-collapse-up</v-icon>  </v-tab>
          </v-tabs>

          <v-tabs-items v-model="tab">
            <v-tab-item v-for="i in 3" :key="i" :value="'tab-' + i">
              <v-card flat><v-card-text>{{ text }}</v-card-text></v-card>
            </v-tab-item>
          </v-tabs-items>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>


<script>
import SlovnikSeznam from "./components/SlovnikSeznam.vue";
import MyMenu from "./components/Menu.vue";

export default {
  name: "app",
  data() {
    return {
      danie: "Danie",
      right: null,
      tab: null,
      text: 'lopem'
    };
  },
  components: { SlovnikSeznam, MyMenu },
  created() {},
  mounted() {},
};
</script>




<style scoped>
</style>