<template>
  <div class="mypage">
    <h1 class="title">MyPage</h1>
    <div class="profile-area">
      <p v-on:click="countUp">{{ aaa }}{{ count }}</p>
      <ul>
        <li v-for="(text, index) in texts" :key="index">{{ text.title }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'mypage',
  data: function () {
    return {
      aaa: 'aaaa',
      count: 0,
      texts: []
    }
  },
  methods: {
    countUp: function () {
      this.count++
      axios.get('https://hn.algolia.com/api/v1/search?query=react').then(res => {
        this.texts = res.data.hits
        console.log(res.data.hits)
      })
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
