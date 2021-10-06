<template>
  <div class="form-group">
    <hr style="border:2px solid #aaa">
    <h3>これまでのツイーヨ</h3>
    <div v-for="(item,key) in tweets" :key="key">
      <dir class="user">{{`${item.tweet_user.user_name}@${item.tweet_user.user_id}`}}</dir>
      <p class="tweet">{{item.tweet_body}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'tweet',
  props: {
    msg: String
  },
  data() {
    return {
      tweets:[
        {tweet_id:1,tweet_user:{user_id:"testId",user_name:"testUser"},tweet_body:"おはよう"},
        {tweet_id:2,tweet_user:{user_id:"testId",user_name:"testUser"},tweet_body:"こんにちは"},
        {tweet_id:3,tweet_user:{user_id:"testId",user_name:"testUser"},tweet_body:"こんばんは"},
      ]
    }
  },
}
</script>
<style>
  .user{
    border: 2px solid #444;;
    font-size: 1.3em;
    text-align: left;
    width: 40%;
    border-bottom: transparent;
    border-top-right-radius: 10px;
    border-top-left-radius: 10px;
    margin: 0;
    padding: 0 0 0 0.5em;
    background-color: #070a;
    color: white;
  }
  .tweet{
    border: 2px solid #444;
    height: 110px;
    margin: 0 0 1em 0;
    padding: 0.5em 0 0 0.4em;
    text-align: left;
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
    border-bottom-left-radius: 10px;
    background-color: #6f65;
  }
  
</style>
