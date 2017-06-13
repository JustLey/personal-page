<template>
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
</template>

<script>
export default {
  name: 'bye',
  data () {
    return {
      hovered: false
    }
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
</style>
