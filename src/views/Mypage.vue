<template>
  <div class="mypage">
    <h1 class="title">MyPage</h1>
    <div class="profile-area">
      <p v-on:click="countUp">{{ aaa }}{{ count }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'mypage',
  data: function () {
    return {
      aaa: 'aaaa',
      count: 0
    }
  },
  methods: {
    countUp: function () {
      this.count++
    }
  }
}
</script>

<style scoped>
  .title {
    color: pink;
  }
  .profile-area {
    height: 300px;
    border-radius: 4px;
    border: 1px solid rgb(243, 242, 242);
  }
</style>
