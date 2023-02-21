<template>
  <div class="home">
    <NavbarView />
    <ContentView />
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarView from '@/components/NavbarView.vue'
import ContentView from '@/components/ContentView.vue'

export default {
  name: 'MainView',
  components: {
    NavbarView,
    ContentView
  }
}
</script>
