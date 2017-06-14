<template>
  <footer>

  <div class="bye">
    Powered by
    <div>
      <img @mouseover="hovered = true" id="icon" src="../assets/logo.png" width="24px" height="24px">
      <transition name="slide-fade">
        <span id="framework-name" v-if="hovered">
          <a href="https://vuejs.org">
            Vuejs
          </a>
        </span>
      </transition>
    </div>
  </div>
  <div><span style="vertical-align: middle;">Você pode conferir o código-fonte dessa página no </span><a href="https://github.com/JustLey/personal-page"><btn style="vertical-align: middle;" icon="github"></btn></a></div>
</footer>
</template>

<script>
import Btn from '@nylira/vue-button'

export default {
  name: 'bye',
  data () {
    return {
      hovered: false
    }
  },
  components: {
    Btn
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
  height: 100%;
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active for <2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
#framework-name {
  display: block;
}

footer {
  padding-top: -20px;
}
</style>
