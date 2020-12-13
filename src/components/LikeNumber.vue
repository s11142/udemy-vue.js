<template>
  <div>
    <p>いいね( {{ halfNumber }} )</p>
    <button @click="increment">+1</button>
  </div>
</template>

<script>
  export default {
    props: {
      totalNumber: String //型を指定することでバリデーションチェックを行う。
    },
    computed: {
      halfNumber () {
        return this.totalNumber / 2;d
      }
    },
    methods: {
      increment() {
        this.totalNumber += 1;
      }
    }
  }
</script>

<style scoped>
  div {
    border: 1px solid red !important;
  }
</style>
