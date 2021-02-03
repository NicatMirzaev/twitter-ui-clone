<template>
  <div class="feed">
    <div class="feed-header">
      <span class="home-text">Home</span>
      <StarIcon class="icon" width="24" height="24"/>
    </div>
    <div class="feed-tweet">
      <Profile style="margin-right:10px;cursor:pointer;" src="https://avatars.githubusercontent.com/u/69142696?s=460&u=b9ac388d4a065d8a43189371854639db425b418c&v=4" width="50" height="50"/>
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
      <div style="width:100%;" v-for="post in posts" :key="post">
        <Post :img="post.img" :fullName="post.fullName" :username = "post.username" :publishedAt = "post.publishedAt" :content="post.content" :comments="post.comments" :retweets="post.retweets" :likes="post.likes"></Post>
      </div>
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
  components: { StarIcon, MediaIcon, GifIcon, PollIcon, EmojiIcon, ScheduleIcon, Profile, Post},
  data () {
    return {
      posts: [
        {
          img: "https://avatars.githubusercontent.com/u/69142696?s=460&u=b9ac388d4a065d8a43189371854639db425b418c&v=4",
          fullName: "Nicat Mirzaev",
          username: "@nicat.mirzaev",
          publishedAt: "Feb 3",
          content: "Hello, world!",
          comments: 10,
          retweets: 5,
          likes: 8
        }
      ]
    }
  }
}
</script>

<style scoped>
.feed {
  flex: 0.6;
  display: flex;
  flex-direction: column;
  height: 100vh;
  overflow-y: scroll;
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
  width: 100%;
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
  width: 98%;
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
@media screen and (max-width: 1180px) {
  .feed {
    flex: 0.6;
  }
}
@media screen and (max-width: 895px) {
  .feed {
    flex: 0.9;
  }
}
</style>
