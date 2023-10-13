<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script >
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import { onMounted, ref } from 'vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },

  setup () {
    const enviroment = ref(process.env.VUE_APP_PATH)
    onMounted(() => {
      console.log(process.env.VUE_APP_PATH)
      console.log('message')
      console.log(enviroment.value)
    })

    return {
      enviroment
    }
  }
}

</script>
