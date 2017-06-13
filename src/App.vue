<template>
  <div id="app">
    <hello></hello>
    <technology-list :description.sync="description"></technology-list>
    <bye></bye>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Bye from './components/Bye'
import TechnologyList from './components/TechnologyList'

export default {
  name: 'app',
  components: {
    Hello,
    Bye,
    TechnologyList
  }
}
</script>

<style>

@font-face {
  font-family: 'Lato';
  font-style: normal;
  font-weight: 400;
  src: local('Lato Regular'), local('Lato-Regular'), url(http://fonts.gstatic.com/s/lato/v13/UyBMtLsHKBKXelqf4x7VRQ.woff2) format('woff2');
}

#app {
  font-family: 'Lato', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  display: flex;
  /* Direction of the items, can be row or column */
  flex-direction: column;
}
</style>
