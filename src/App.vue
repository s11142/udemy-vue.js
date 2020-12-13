<template>
  <div>
    <like-Header></like-Header>
    <h2>{{ number }}</h2>
    <like-Number :total-number="number"></like-Number>
    <like-Number :total-number="number"></like-Number>
  </div>
</template>

<script>
  import  LikeHeader  from "./components/LikeHeader.vue";
  import  LikeNumber  from "./components/LikeNumber.vue";

  export default {
    data () {
      return {
        number: 18
      }
    },
    components: {
      LikeHeader,
      LikeNumber
    }
  }
</script>

<style scoped>
  div {
    border: 1px solid blue;
  }
</style>
