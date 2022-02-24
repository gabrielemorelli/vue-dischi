<template>
  <main>
    <div class="container">
      <CardDischi
        v-for="(disco, index) in listaDischi"
        :key="index"
        :disco="disco"
      />
    </div>
  </main>
</template>

<script>
const axios = require("axios");
import CardDischi from "./partials/CardDischi.vue";
export default {
  name: "ListaDischi",
  data() {
    return {
      listaDischi: [],
      loadingInProgress: true,
      endpoint: "https://flynn.boolean.careers/exercises/api/array/music",
    };
  },
  components: {
    CardDischi,
  },
  methods: {
    getDischi() {
      axios
        .get(this.endpoint)

        .then((response) => {
          this.listaDischi = response.data.response;
          this.loadingInProgress = false;
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        })
        .then(function () {
          // always executed
        });
    },
  },
  mounted() {},
  created() {
    this.getDischi();
  
  },
};
</script>

<style>
main {
  background-color: #1e2d3b;
}

.container {
  width: 70%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  min-height: 300px;
  padding: 40px;
}
</style>


    

   
