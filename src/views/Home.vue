<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloNuxt />
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import HelloNuxt from '@/components/HelloNuxt.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    HelloNuxt
  }
}
</script>
