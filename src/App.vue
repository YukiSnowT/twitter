<template>
  <div class="all" style="display:flex;">
    <div class="left" style="width:20%;"></div>
    <div id="form" class="form" style="width:60%;">
      <Form v-on:addTweeyo="setTweeyo"/>
      <Tweet />
    </div>
    <div class="right" style="width:20%;"></div>
  </div>
</template>

<script>
import Form from './components/Form.vue'
import Tweet from './components/Tweet.vue'

export default {
  name: 'App',
  components: {
    Form,
    Tweet
  },
  data(){
    return {

    }
  },
  methods: {
    setTweeyo(msg){
      console.log(msg);
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
