<template>
  <div>
    <like-Header></like-Header>
    <h2>{{ number }}</h2>
    <like-Number :total-number="number" @my-click="incrementNumber"></like-Number>
    <like-Number :total-number="number" :test-props="testProps"></like-Number>
  </div>
</template>

<script>
  import  LikeHeader  from "./components/LikeHeader.vue";
  import  LikeNumber  from "./components/LikeNumber.vue";

  export default {
    data () {
      return {
        number: 18,
        testProps: 'test'
      }
    },
    components: {
      LikeHeader,
      LikeNumber
    },
    methods: {
      incrementNumber (value) {
        this.number = value;
      }
    }
  }
</script>

<style scoped>
  div {
    border: 1px solid blue;
  }
</style>
