<template>
  <div>
    <h1 class="aaaa">Hello Nuxt!{{ msg }}</h1>
    <h1 v-on:click="onclickFunction('しこしこしこ')">{{ aaa }}</h1>
    <input type="text" v-model="aaa">
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      msg: 'aaaaaaaaaaaaa',
      aaa: 'ははは'
    }
  },
  methods: {
    onclickFunction: function (text) {
      this.msg = text
    }
  }
}
</script>

<style scoped>
  .aaaa {
    color: red;
  }
</style>
