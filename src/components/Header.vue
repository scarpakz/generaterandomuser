<template>
  <header>
      <h1>{{ title }}</h1>
      <RandomUsers />
  </header>
</template>

<script>
// import Button from './Button.vue'
import RandomUsers from './RandomUsers.vue'

export default {
    // components:{
    //     Button,
    // },
    components: {
        RandomUsers,
    },
    props: {
        title: String
    }
}
</script>

<style scoped>

</style>