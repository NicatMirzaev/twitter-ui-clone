<template>
  <div class="sidebar">
    <div>
      <TwitterIcon class="twitter-icon" width="30" height="30"/>
      <div class="sidebar-option">
        <HomeIcon class="home-icon" width="28" height="28"/>
        <span class="text active">Home</span>
      </div>
      <div class="sidebar-option">
        <ExploreIcon class="icon" width="28" height="28"/>
        <span class="text">Explore</span>
      </div>
      <div class="sidebar-option">
        <NotificationsIcon class="icon" width="28" height="28"/>
        <span class="text">Notifications</span>
      </div>
      <div class="sidebar-option">
        <MessageIcon class="icon" width="28" height="28"/>
        <span class="text">Messages</span>
      </div>
      <div class="sidebar-option">
        <BookmarkIcon class="icon" width="28" height="28"/>
        <span class="text">Bookmarks</span>
      </div>
      <div class="sidebar-option">
        <ListIcon class="icon" width="28" height="28"/>
        <span class="text">Lists</span>
      </div>
      <div class="sidebar-option">
        <ProfileIcon class="icon" width="28" height="28"/>
        <span class="text">Profile</span>
      </div>
      <div class="sidebar-option">
        <MoreIcon class="icon" width="28" height="28"/>
        <span class="text">More</span>
      </div>
      <div class="button">
        <span class="button-text">
          Tweet
        </span>
        <TweetIcon class="tweet-icon" width="24" height="24"/>
      </div>
    </div>
    <div class="profile">
      <Profile style="margin-right:10px;" src="https://avatars.githubusercontent.com/u/69142696?s=460&u=b9ac388d4a065d8a43189371854639db425b418c&v=4" width="40" height="40"/>
      <div class="user_info">
        <span class="name">Nicat Mirzaev</span>
        <span class="username">@nicat.mirzaev</span>
      </div>
      <MoreIcon2 class="more-icon" width="24" height="24"/>
    </div>
  </div>
</template>
<script>

import TwitterIcon from '../icons/Twitter.vue';
import HomeIcon from '../icons/Home.vue';
import ExploreIcon from '../icons/Explore.vue';
import NotificationsIcon from '../icons/Notifications.vue';
import MessageIcon from '../icons/Message.vue';
import BookmarkIcon from '../icons/Bookmark.vue';
import ListIcon from '../icons/List.vue';
import ProfileIcon from '../icons/Profile.vue';
import MoreIcon from '../icons/More.vue';
import Profile from './Profile.vue';
import MoreIcon2 from '../icons/More2.vue';
import TweetIcon from '../icons/Tweet.vue';
export default {
  name: 'Sidebar',
  components: { TwitterIcon, HomeIcon, ExploreIcon, NotificationsIcon, MessageIcon, BookmarkIcon, ListIcon, ProfileIcon, MoreIcon, Profile, MoreIcon2, TweetIcon}
}

</script>

<style scoped>
.tweet-icon {
  display: none;
}
.sidebar {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  flex: 0.1;
  height: 95vh;
  padding: 20px;
}
.sidebar-option {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
  padding-left: 10px;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-right: 10px;
}
.twitter-icon:hover {
  background-color: #deefff;
  border-radius: 9999px;
}
.twitter-icon {
  margin-bottom: 15px;
  cursor: pointer;
  padding-left: 10px;
  padding-right: 10px;
  fill: #1DA1F2;
}
.home-icon {
  cursor: pointer;
  fill: #1DA1F2;
}
.sidebar-option:hover .text {
  color: #1DA1F2;
}
.sidebar-option:hover .icon {
  fill: #1DA1F2;
}
.sidebar-option:hover {
  background-color: #deefff;
  border-radius: 999px;
}
.icon {
  cursor: pointer;
}
.active {
  color: #1DA1F2;
}
.text {
  font-size: 19px;
  cursor: pointer;
  font-weight: 700;
  line-height: 25px;
  margin-left: 20px;
}
.button:hover {
  background-color: #2190e2;
}
.button:focus {
  border: none;
  outline: none;
  border-width: 0px;
}
.button-text {
  font-size: 15px;
  font-weight: 700;
  color: white;
  padding-top: 15px;
  padding-bottom: 15px;
}
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  background-color: #1DA1F2;
  width: 230px;
  border-radius: 9999px;
  border-width: 1px;
  margin-top: 15px;
}
.profile:hover {
  background-color: #deefff;
  border-radius: 999px;
}
.profile {
  cursor: pointer;
  margin-left: 10px;
  margin-top: 10px;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}
.name {
  font-size: 15px;
  font-weight: 700;
  line-height: 20px;
  color: #0f1419;
}
.username {
  font-size: 15px;
  font-weight: 400;
  line-height: 20px;
  color: #5b7083;

}
.user_info {
  display: flex;
  flex-direction: column;
  margin-right: 100px;
}
@media screen and (max-width: 1185px) {
  .text {
    display: none;
  }
  .sidebar {
    max-width: 50px;
  }
  .button {
    width: 50px;
  }
  .button-text {
    display: none;
  }
  .tweet-icon {
    display: inline-block;
    fill: white;
    padding-top: 15px;
    padding-bottom: 15px;
  }
  .profile {
    width: 50px;
    margin: 0;
  }
  .user_info {
    display: none;
  }
  .more-icon {
    display: none;
  }
}
</style>
