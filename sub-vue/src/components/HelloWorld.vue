<template>
  <div class="hello">
    <span @click="changeName" class="change">修改名字</span>
  </div>
</template>

<script>
import store from '../store';

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    changeName(){
      store.dispatch('global/setGlobalState', {
        user: {
          name: 'lisi'
        }
    })
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
.change{
  cursor: pointer;
}
</style>
