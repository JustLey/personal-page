<template>
  <div id="app">
    <hello></hello>
    <technology name="Ruby"
                icon="https://cdn.codementor.io/assets/topic/category_header/ruby-on-rails-bc9ab2af8d92eb4e7eb3211d548a09ad.png"
                site="https://www.ruby-lang.org"
                color="#d73a2e"
                ></technology>
    <technology name="Cache"
                icon="http://www.intersystems.com/assets/cropped-BRANDMARK_sq_644x644-300x300.png"
                site="http://www.intersystems.com/our-products/cache/cache-overview/"
                color="#26308a"
                ></technology>
    <bye></bye>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Bye from './components/Bye'
import Technology from './components/Technology'

export default {
  name: 'app',
  components: {
    Hello,
    Bye,
    Technology
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
