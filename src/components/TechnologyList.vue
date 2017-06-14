<template>
  <div style="margin: 16px; flex: 1">
  <div class="technology-list">
    <h3>Experiência</h3>
    <technology name="Ruby"
                icon="https://cdn.codementor.io/assets/topic/category_header/ruby-on-rails-bc9ab2af8d92eb4e7eb3211d548a09ad.png"
                site="https://www.ruby-lang.org"
                color="#d73a2e"
                description="Ruby é uma linguagem interpretada que segue os paradigmas de orientação à objeto à risca. Desenvolvo a 3 anos na mesma, tendo utilizado em projetos como Laissez e Doctorpedia."
                v-on:changeParentDescription="changeDescription"
                ></technology>
    <technology name="Cache"
                icon="http://www.intersystems.com/assets/cropped-BRANDMARK_sq_644x644-300x300.png"
                site="http://www.intersystems.com/our-products/cache/cache-overview/"
                color="#26308a"
                description="Caché trata-se de um sistema de gerencia de banco de dados relacional. Possui diversas aplicações na àrea da saúde por ser rápido e robusto. Possuo 7 anos de experiencia no mesmo, tendo prestado serviços ao Tribunal de Justiça de Santa Catarina mantendo seus sistemas desenvolvidos nesta tecnologia atualizados."
                v-on:changeParentDescription="changeDescription"
                ></technology>
    <technology name="Vue.js"
                icon="https://avatars3.githubusercontent.com/u/6128107?v=3&s=400"
                site="http://www.vuejs.org"
                color="#42b98"
                description="Vue.js é um framework front-end reativo, performático e declarativo desenvolvido pelo ex-Googler Evan You. Possuo 4 meses de experiencia no mesmo, tendo desenvolvido parte do meu projeto (Laissez) utilizando-o. Esta página também é desenvolvida em Vue.js"
                v-on:changeParentDescription="changeDescription"
                ></technology>
              </div>
    <div id="description" style="margin-top: 64px">
      <transition name="slide-fade" appear>
        <h4>{{ description }}</h4>
      </transition>
    </div>
</div>
</template>

<script>
import Technology from './Technology'

export default {
  name: 'technology-list',
  props: {
    description: {
      type: String,
      default: 'Passe o mouse sobre uma tecnologia para saber mais'
    }
  },
  data () {
    return {
      description: this.description
    }
  },
  components: {
    Technology
  },
  methods: {
    changeDescription: function (e) {
      this.description = e
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

h4 {
  font-weight: 500;
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

#description {
  margin: 16px 512px;
  text-align: center;
}

@media screen and (max-width: 1304px) {
  #description {
    margin: 16px 350px;
    text-align: center;
  }
}

@media screen and (max-width: 1024px) {
  #description {
    margin: 16px 300px;
    text-align: center;
  }
}

@media screen and (max-width: 768px) {
  #description {
    margin: 16px 256px;
    text-align: center;
  }
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
</style>
