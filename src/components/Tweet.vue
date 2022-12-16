<template>
  <div class="tweet">

    <ProfileImage :image="tweet.user.image" />
    <!-- <img
      :src="tweet.user.image"
      class="profile"
      alt="profile"
    /> -->

    <div class="body">
      <div class="top">
        
        <User :user="tweet.user"/>
        <!-- <span class="user">
          <span class="name">{{ tweet.user.name }}</span>
          <span class="handle">{{ tweet.user.handle }}</span>
        </span> -->

        <Timestamp :timestamp="tweet.timestamp" />
        <!-- <span class="timestamp">{{ tweet.timestamp }}</span> -->
      </div>

      <Message :message="tweet.message" />
      <!-- <p class="message">{{ tweet.message }}</p> -->

      <Actions />
      <!-- <div class="actions">
         Font Awesome icons 
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
        <i class="fas fa-ellipsis-h"></i>
      </div> -->
    </div>

  </div>
</template>
<script>
  import Message from './Message.vue'; 
  import Timestamp from './Timestamp.vue';
  import ProfileImage from './ProfileImage.vue';
  import User from './User.vue';
  import Actions from './Actions.vue';

  export default {
    props: {tweet:Object},
    components: {
      Message, Timestamp, ProfileImage, User, Actions 
    }
  }
</script>
<style scoped>
a {
  color: #42b983;
}
</style>
