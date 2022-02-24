<template>
  <div class="card" >
        <img :src="disco.poster" />
        <h2>{{disco.title}}</h2>
        <div>{{disco.author}}</div>
        <div>{{disco.year}}</div>
      </div>
</template>

<script>
export default {
name:'CardDischi',
props:{
    "disco" : Object 
}
}
</script>

<style scoped lang="scss">
.card {
  width: 15%;
  min-height: 250px;
  padding: 10px;
  background-color: #2e3a46;


  img{
    width: 100%;
  }
}
</style>