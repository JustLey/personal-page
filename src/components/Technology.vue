<template>
  <div class="technology" style="margin: 16px">
    <div>
      <img @mouseover="changeParentDescription" id="icon" :src="icon" width="24px" height="24px">
      <transition name="slide-fade">
        <span id="technology-name" v-if="hovered" style="display: block">
          <a :href="site" :style="{ color: color }">
            {{ name }}
          </a>
        </span>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: 'technology',
  props: {
    name: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      required: true
    },
    site: {
      type: String,
      required: true
    },
    color: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  },
  data () {
    return {
      name: this.name,
      icon: this.icon,
      site: this.site,
      hovered: false,
      color: this.color,
      description: this.description
    }
  },
  methods: {
    changeParentDescription: function() {
      this.hovered = true
      this.$emit('changeParentDescription', this.description)
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

#technology-name a {
  text-decoration: none;
}

.technology {
  display: inline-block;
}

</style>
