<script setup>

//--------importing all components of the tweet-----------
import Actions from './Actions.vue';
import Message from './Message.vue';
import ProfileImage from './ProfileImage.vue';
import Timestamp from './Timestamp.vue';
import User from './User.vue';


defineProps({
  tweet: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <!--showing the tweet components by referencing their respective object-->
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :user="tweet.user" />
         <Timestamp :timestamp="tweet.timestamp" /> 
      </div>
      <br>
      <Message :message="tweet.message" /> 
      <Actions></Actions>

    </div>

    <i class="fas fa-ellipsis-h"></i>

  </div>
</template>


