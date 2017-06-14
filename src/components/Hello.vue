<template>
  <div class="hello">
    <div id="picture">
      <img src="https://scontent.ffln1-1.fna.fbcdn.net/v/t1.0-1/c0.13.160.160/p160x160/12742039_1235835416444181_3921745145941891349_n.jpg?oh=7e56d259a107470d603619501e7f4cca&oe=59D8774F" width="144px" height="144px">
    </div>
    <div id="info">
      <h1>Rian Provesano Reis</h1>
      <h4>
        <span>Desenvolvedor, Graduando de Sistemas de Informação, Empreendedor e Entusiasta Eclético</span>
        <br>
        <span>Fundador @ <a href="https://laissez.io"> laissez.io</a></span>
        <br>
        <span><a href="https://docs.google.com/document/d/1i6IGCnA3VLk3b4y6rTe5Wh-d4xEmVtDe7-WOc_Pq6Lk/pub">Curriculum Vitae</a></span>
        <btn icon="email"></btn><span>rianreis@outlook.com</span>
      </h4>
      <a href="https://www.linkedin.com/in/rian-provesano-reis-431a9932/">
        <btn icon="linkedin" theme="tendermint" size="lg"></btn>
      </a>
      <a href="https://www.github.com/JustLey/">
        <btn icon="github" theme="alpha-black" size="lg"></btn>
      </a>
      <a href="https://www.facebook.com/rian.provesanoreis">
        <btn icon="facebook" theme="tendermint" size="lg"></btn>
      </a>
    </div>
  </div>
</template>

<script>
import Btn from '@nylira/vue-button'

export default {
  name: 'hello',
  data () {
    return {
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
  font-weight: 500;
  font-size: 32px;
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
}

#picture {
  display: block;
}

#picture > img {
  border-radius: 50%;
  crop: center;
}

#info {
  display: block;
  margin-left: 8px;
}

.ni-btn-wrapper {
  display: inline-block;
}

.ni-btn {
  background: #f00;
}

h4 {
  font-weight: 400;

}
.hello {

  margin-top: 30px;
}
</style>
