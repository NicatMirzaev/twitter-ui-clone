<template>
  <div class="widgets">
    <div class="input-container">
      <SearchIcon class="icon" style="padding-left:5px;" width="40" height="18"/>
      <input class="input" placeholder="Search Twitter"/>
    </div>
    <div class="trends">
      <div class="trends-header">
        <span class="trends-for-you">Trends for you</span>
        <SettingsIcon fill="#1DA1F2" style="padding-right:5px;cursor:pointer;" width="22" height="22"/>
      </div>
      <div class="trend-content">
        <div class="content-header">
          <span class="header-text">Trending in Georgia</span>
          <MoreIcon2 style="cursor:pointer" width="18" height="18"/>
        </div>
        <span class="content-hashtag">#1yearofwalls</span>
        <span style="padding-left:15px;margin-bottom:10px;" class="header-text">166K Tweets</span>
      </div>
      <span class="show-more">Show More</span>
    </div>
    <div class="follow">
      <span style="margin-bottom: 10px; margin-top: 5px;" class="trends-for-you">Who to follow</span>
      <div class="follow-card">
        <Profile style="margin-right:20px;" src="https://static.thenounproject.com/png/630740-200.png" width="40" height="40"/>
        <div class="names">
          <span class="fullname">Elon Musk</span>
          <span class="username">@elon.musk</span>
        </div>
        <button class="follow-button">Follow</button>
      </div>
      <div class="follow-card">
        <Profile style="margin-right:20px;" src="https://static.thenounproject.com/png/630740-200.png" width="40" height="40"/>
        <div class="names">
          <span class="fullname">Elon Musk</span>
          <span class="username">@elon.musk</span>
        </div>
        <button class="follow-button">Follow</button>
      </div>
      <div class="follow-card">
        <Profile style="margin-right:20px;" src="https://static.thenounproject.com/png/630740-200.png" width="40" height="40"/>
        <div class="names">
          <span class="fullname">Elon Musk</span>
          <span class="username">@elon.musk</span>
        </div>
        <button class="follow-button">Follow</button>
      </div>
      <span class="show-more">Show More</span>
    </div>
  </div>
</template>

<script>
import SearchIcon from '../icons/Search';
import SettingsIcon from '../icons/Settings';
import MoreIcon2 from '../icons/More2';
import Profile from './Profile.vue';

export default {
  name: 'Widgets',
  components: { SearchIcon, SettingsIcon, MoreIcon2, Profile }
}
</script>

<style scoped>
.widgets {
  flex: 0.3;
  display: flex;
  flex-direction: column;
}
.icon {
  fill: rgb(91, 112, 131);
}
.input-container {
  margin-left: 20px;
  margin-top: 10px;
  width: 100%;
  height: 42px;
  display: flex;
  align-items: center;
  background-color: #EBEEF0;
  border-radius: 999px;
}
.follow-card {
  display: flex;
  align-items: center;
  padding: 10px;
  cursor: pointer;
  border-top: 1px solid #EBEEF0;
}
.follow-card:hover {
  background-color: #EBEEF0;
}
.names {
  display: flex;
  flex-direction: column;
  margin-right: auto;
}
.follow-button {
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 5px;
  padding-bottom: 5px;
  border-radius: 16px;
  border: 1px solid #ccc;
  background-color: white;
  font-size: 15px;
  font-weight: 700;
  line-height: 20px;
  color: #1DA1F2;
  cursor: pointer;
  border-color: rgb(29, 161, 242)
}
.follow-button:hover {
  background-color: #EBEEF0;
}
.trends-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding-bottom: 5px;
  margin-bottom: 5px;
  margin-top: 5px;
}
.trends {
  margin-left: 20px;
  margin-top: 20px;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: rgb(247, 249, 250);
  border-radius: 16px;
}
.follow {
  display: flex;
  flex-direction: column;
  background-color: rgb(247, 249, 250);
  border-radius: 16px;
  width: 100%;
  margin-left: 20px;
  margin-top: 30px;
}
.trends-for-you {
  font-size: 19px;
  line-height: 25px;
  font-weight: 800;
  padding-left: 15px;
  padding-right: 15px;
}
.trend-content {
  display: flex;
  flex-direction: column;
  border-bottom: 1px solid #EBEEF0;
  cursor: pointer;
  border-top: 1px solid #EBEEF0;
}
.trend-content:hover {
  background-color: #EBEEF0;
}
.content-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-left: 15px;
  padding-right: 10px;
  padding-top: 5px;
  margin-bottom: 3px;
}
.header-text {
  font-size: 13px;
  font-weight: 400;
  line-height: 20px;
  color: #5b7083;
}
.show-more {
  font-size: 15px;
  font-weight: 400;
  line-height: 20px;
  color: #1DA1F2;
  padding: 15px;
  cursor: pointer;
  border-top: 1px solid #EBEEF0;
  border-bottom-right-radius: 16px;
  border-bottom-left-radius: 16px;
}
.show-more:hover {
  background-color: #EBEEF0;
}
.fullname {
  font-size: 15px;
  font-weight: 700;
  line-height: 20px;
}
.username {
  font-size: 15px;
  font-weight: 400;
  line-height: 20px;
  color: #5b7083;
}
.content-hashtag {
  font-size: 15px;
  font-weight: 700;
  line-height: 20px;
  padding-left: 15px;
  margin-bottom: 3px;
}
.input-container:focus-within {
  border: 1px solid #1DA1F2;
  background-color: white;
}
.input-container:focus-within .icon {
  fill: #1DA1F2;
}
.input {
  background-color: inherit;
}
.input:focus {
  border: none;
  outline: none;
  border-width: 0px;
}
</style>
