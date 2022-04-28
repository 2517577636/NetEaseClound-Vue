<template>
  <div class="home">
    <navList :list="list"></navList>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import navList from "@/components/navlist/index.vue"

export default {
  name: 'HomeView',
  data() {
    return {
      list: [
        {
          text: "推荐音乐",
        },
        {
          text: "发现音乐",
        },
        {
          text: "关注",
        }
      ]
    }
  },

  components: {
    navList
  }
}
</script>
