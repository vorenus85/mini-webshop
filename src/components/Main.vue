<template>
  <div class="header">
    <h1>Mini-webshop with Vue.js</h1>
    <div class="container">
      <div class="row">
        <div class="shop-item col-md-3 col-sm-6"
             v-for="data in myJson"
             :key="data.id">
          <span class="shop-item-name">{{data.name}}</span>
          <img :src="data.imgUrl" class="img-fluid"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import json from '../json/data.json'
export default {
  name: 'Main',
  data () {
    return {
      myJson: json,
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  h1,
  h2 {
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
  }
</style>
