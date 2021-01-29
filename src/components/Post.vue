<template>
  <div class="post">
    <Profile style="margin-right:10px;cursor:pointer;" src="https://static.thenounproject.com/png/630740-200.png" width="50" height="50"/>
    <div class="post-content">
      <div class="post-header">
        <div>
          <span class="fullname">Nicat Mirzoev</span>
          <span class="username">@nicat.mirzoev</span>
          <span style="margin-left:5px;margin-right:5px;">·</span>
          <span class="username">Jan 25</span>
        </div>
        <MoreIcon2 style="cursor:pointer;" width="24" height="24"/>
      </div>
      <span class="content-text">"gençlerin hayatındaki kaygıların/endişelerin yarısı belirsiz ilişkilerden kaynaklanıyor" -- ilişkilerimizde net değiliz. çevremizdeki insanlara onlardan beklentimizi ifade edemiyoruz. faydası olmayan insanlarla fazla alakadarız ve bu hayatı lüzumsuz yere zorlaştırıyor.</span>
      <div class="post-footer">
        <div style="display:flex;">
          <CommentIcon class="icon" width="19" height="19"/>
          <span class="text">20</span>
        </div>
        <div style="display:flex;">
          <RetweetIcon class="icon" width="19" height="19"/>
          <span class="text">126</span>
        </div>
        <div style="display:flex;">
          <LikeIcon class="icon" width="19" height="19"/>
          <span class="text">1.7k</span>
        </div>
        <SendIcon class="icon" width="19" height="19"/>
      </div>
    </div>
  </div>
</template>

<script>
import Profile from './Profile.vue';
import MoreIcon2 from '../icons/More2.vue';
import CommentIcon from '../icons/Comment.vue';
import RetweetIcon from '../icons/Retweet.vue';
import LikeIcon from '../icons/Like.vue';
import SendIcon from '../icons/Send.vue';
export default {
  name: 'Post',
  components: { Profile, MoreIcon2, CommentIcon, RetweetIcon, LikeIcon, SendIcon },
  props: {
    img: String,
    fullName: String,
    username: String,
    publishedAt: String,
    content: String,
    comments: Number,
    retweets: Number,
    likes: Number
  }
}
</script>

<style scoped>
.post {
  padding: 10px;
  display: flex;
  border-right: 1px solid #EBEEF0;
  border-bottom: 1px solid #EBEEF0;
  border-left: 1px solid #EBEEF0;
}
.post-content {
  display: flex;
  flex-direction: column;
}
.icon {
  fill: rgb(91, 112, 131);
  margin-right: 5px;
  cursor: pointer;
  padding: 5px;
}
.icon:hover {
  background-color: #deefff;
  border-radius: 999px;
}
.post-header {
  display: flex;
  justify-content: space-between;
  width: 40vw;
}
.post-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.fullname {
  font-size: 15px;
  line-height: 20px;
  font-weight: 700;
  margin-right: 5px;
}
.username {
  font-size: 15px;
  line-height: 20px;
  font-weight: 400;
  color: #5b7083;
}
.text {
  font-size: 13px;
  font-weight: 400;
  color: rgb(91, 112, 131);
  padding: 5px;
}
.content-text {
  font-size: 15px;
  font-weight: 400;
  line-height: 20px;
  margin-bottom: 15px;
}
</style>
