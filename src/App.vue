<template>
  <div id="app">
    <MyHeader/>
    <ListaDischi />
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue";
import ListaDischi from "./components/ListaDischi.vue";


export default {
  name: "App",
  components: {
    MyHeader,
    ListaDischi,
  },
  data(){
  
  }
}
</script>

<style lang="scss">

 @import './style/general.scss';
 
</style>
