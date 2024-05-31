<script setup>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import TimeStamp from "./TimeStamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue"; 

defineProps({
  tweet: Object,
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />
    <div class="body">
      <div class="top">
        <span class="user">
          <User :userData="tweet.user" />
        </span>
        <span class="timestamp">
          <TimeStamp :time="tweet.timestamp" />
        </span>
      </div>
      <Message :message="tweet.message" />
      <div class="actions">
        <Actions />
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
