<template>
  <div class="feed">
    <div class="feed-header">
      <span class="home-text">Home</span>
      <StarIcon class="icon" width="24" height="24"/>
    </div>
    <div class="feed-tweet">
      <Profile style="margin-right:10px;cursor:pointer;" src="https://static.thenounproject.com/png/630740-200.png" width="50" height="50"/>
      <div class="feed-tweet2">
        <input class="input" placeholder="What's happening?"/>
        <div class="feed-tweet-footer">
          <div>
            <MediaIcon style="margin-right:10px;" class="icon" width="24" height="24"/>
            <GifIcon style="margin-right:10px;" class="icon" width="24" height="24"/>
            <PollIcon style="margin-right:10px;" class="icon" width="24" height="24"/>
            <EmojiIcon style="margin-right:10px;" class="icon" width="24" height="24"/>
            <ScheduleIcon class="icon" width="24" height="24"/>
          </div>
          <button class="button">Tweet</button>
        </div>
      </div>
    </div>
    <div class="posts">
      <Post/>
      <Post/>
      <Post/>
      <Post/>
      <Post/>
      <Post/>
    </div>
  </div>
</template>

<script>
import StarIcon from '../icons/Star.vue';
import MediaIcon from '../icons/Media.vue';
import GifIcon from '../icons/Gif.vue';
import PollIcon from '../icons/Poll.vue';
import EmojiIcon from '../icons/Emoji.vue';
import ScheduleIcon from '../icons/Schedule.vue';
import Profile from './Profile.vue';
import Post from './Post.vue';

export default {
  name: 'Feed',
  components: { StarIcon, MediaIcon, GifIcon, PollIcon, EmojiIcon, ScheduleIcon, Profile, Post}
}
</script>

<style scoped>
.feed {
  flex: 0.5;
  display: flex;
  flex-direction: column;
  height: 100vh;
  overflow-y: scroll;
  min-width: 760px;
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */
}
.feed::-webkit-scrollbar {
    display: none;
}

.icon {
  fill: #1DA1F2;
  cursor: pointer;
}
.feed-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 15px;
  padding-right: 15px;
  border-right: 1px solid #EBEEF0;
  border-bottom: 1px solid #EBEEF0;
  border-left: 1px solid #EBEEF0;
}
.feed-tweet {
  padding: 10px;
  display: flex;
  border-right: 1px solid #EBEEF0;
  border-bottom: 1px solid #EBEEF0;
  border-left: 1px solid #EBEEF0;
}
.feed-tweet2 {
  padding-top: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.home-text {
  font-size: 19px;
  line-height: 25px;
  font-weight: 800;
}
.input:focus {
  border: none;
  outline: none;
  border-width: 0px;
}
.feed-tweet-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 38vw;
}
.input {
  font-size: 19px;
  font-weight: 400;
  line-height: 25px;
  width: 35vw;
  margin-bottom: 20px;
}
.button {
  font-size: 15px;
  font-weight: 700;
  color: white;
  cursor: pointer;
  background-color: #1DA1F2;
  width: 100px;
  border-radius: 9999px;
  border-width: 1px;
  padding-left: 15px;
  padding-right: 15px;
  padding-top: 10px;
  padding-bottom: 10px;
}
.button:hover {
  background-color: #2190e2;
}
.button:focus {
  border: none;
  outline: none;
  border-width: 0px;
}
.posts {
  display: flex;
  flex-direction: column;
}
</style>
