<template>
  <div>
    <v-card flat>
      <v-card-text>
        <v-text-field v-model="text" label="slovo pro preklad" hide-details="auto" ></v-text-field>
      </v-card-text>
      <v-card-actions>
          <v-spacer></v-spacer>
        <v-btn 
            @click="translate" :disabled="text?false:true" 
            :elevation="5" color="pink"> Přelož </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>


<script>
export default {
  data() {
    return {
      text:""
    }
  },
  // computed: {
  //   disable:
  // },
  methods: {
    translate() {
      var url = "https://slovnik.seznam.cz/preklad/cesky_rusky/" + this.text;
      window.open(url)
    }
  },
};
</script>


<style scoped>

</style>