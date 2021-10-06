<template>
  <div class="form-group" >
    <textarea v-model="tweet" row="5" col="10" class="form-control" placeholder="いま何してる？" style="background-color:#6f68;" v-on:keydown="type"></textarea>
    <button class="btn btn-success text-white mt-2" v-on:click="tweeyo">ツイーヨする</button>
  </div>
</template>

<script>
export default {
  name: 'Form',
  props: {
    msg: String
  },
  methods: {
    tweeyo(){
      this.$emit("addTweeyo",this.msg)
      console.log(this.msg)
    }
  },
}
</script>
