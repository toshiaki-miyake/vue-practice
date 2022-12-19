<script setup>
  import AppHeader from './components/AppHeader.vue'
  import AppSidebar from './components/AppSidebar.vue'
  import AppArticle from './components/AppArticle.vue'
  import AppFooter from './components/AppFooter.vue'

  const removeTodo = (a) => {
    console.log(a)
  }

</script>

<template>
  <AppHeader color="red" @removeTodo="removeTodo('OK')" />

  <main>
    <AppArticle />
    <AppSidebar />
  </main>
  <AppFooter backgroundColor="skyBlue">2022</AppFooter>
</template>