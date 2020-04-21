<template lang="html">
  <li><img v-bind:src="tweet.img" alt="Image of User"><p>{{tweet.name}} {{tweet.handle}}</p>
    <h3>{{tweet.tweet}}</h3><br>
    <p>Likes:{{tweet.likes}}</p>
  </li>
</template>

<script>
export default {
  name: 'tweet-list-item',
  props: ['tweet']
}
</script>

<style lang="css" scoped>

li {
  background-color: #30475e;
  color: white;
  list-style: none;
}

h3 {
  margin-left: 45px;
}

p {
  margin-left: 10px;
}

img {
  border-radius: 50%;
  height: 8%;
  width: 8%;
  margin-top: 5px;
  margin-left: 5px;

}

</style>
