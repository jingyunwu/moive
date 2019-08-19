<template>
  <div id="app">
    <VHeader/>
    <div class="content">
      <KeepAlive :exclude="exclude">
        <RouterView/>
      </KeepAlive>
    </div>
  </div>
</template>

<script>
import VHeader from './components/Header'
export default {
  name: 'App',
  components: {
    VHeader
  },
  data () {
    return {
      exclude: ['User', 'Movie']
    }
  }
}
</script>

<style lang="stylus" scoped>
.content
  position absolute
  top 56px
  bottom 0
  width 100%
</style>