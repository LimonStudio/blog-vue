<template>
  <div class="app">
    <b-header></b-header>
    <router-view/>
    <b-footer></b-footer>
  </div>
</template>

<script>
import BHeader from './components/b-header'
import BFooter from './components/b-footer'
export default {
  components: {
    BHeader,
    BFooter
  }
}
</script>

<style scoped>

</style>
