<template>
  <div>
    <p>いいね( {{ halfNumber }} )</p>
    <p>{{ testProps }}</p>
    <button @click="increment">+1</button>
  </div>
</template>

<script>
  export default {
    props: {
      // totalNumber: Number 型を指定することでバリデーションチェックを行う。Stringが入っていた場合検証ツールにエラー出るよ。
      totalNumber: {
        type: Number,
        required: true,
      },
      testProps: {
        type: String,
        default: 'shota'
      }
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
