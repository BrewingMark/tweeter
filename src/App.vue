<template lang="html">
  <div class="">

    <h1>Tweets</h1>
    <h2>Total Likes:{{totalLikes}}</h2>
    <tweet-list-item v-for="(tweet, index) in tweets" :key="index" :tweet="tweet"></tweet-list-item>

  </div>
</template>

<script>

import TweetListItem from './components/TweetListItem.vue';

export default {
  name: 'app',
  data() {
  return {
    tweets:[
      {
        id: 1,
        name: 'James',
        handle: '@jokerjames',
        img: 'https://semantic-ui.com/images/avatar2/large/matthew.png',
        tweet: "If you don't succeed, dust yourself off and try again.",
        likes: 10,
      },
      {
        id: 2,
        name: 'Fatima',
        handle: '@fantasticfatima',
        img: 'https://semantic-ui.com/images/avatar2/large/molly.png',
        tweet: 'Better late than never but never late is better.',
        likes: 12,
      },
      {
        id: 3,
        name: 'Xin',
        handle: '@xeroxin',
        img: 'https://semantic-ui.com/images/avatar2/large/elyse.png',
        tweet: 'Beauty in the struggle, ugliness in the success.',
        likes: 18,
      }
    ]
  };
},
computed: {
  totalLikes: function(){
  return this.tweets.reduce((runningTotal, tweet) => {
    return runningTotal + tweet.likes;
  }, 0);
}
},
  components: {
    'tweet-list-item': TweetListItem
  }
}
</script>

<style lang="css" scoped>
</style>
