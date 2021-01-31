<template>
  <div class="widgets">
    <div class="input-container">
      <SearchIcon class="icon" style="padding-left:5px;" width="40" height="18"/>
      <input class="input" placeholder="Search Twitter"/>
    </div>
    <div class="trends">
      <span class="trends-for-you">Trends for you</span>
    </div>
  </div>
</template>

<script>
import SearchIcon from '../icons/Search';

export default {
  name: 'Widgets',
  components: { SearchIcon }
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
.trends {
  margin-left: 20px;
  margin-top: 20px;
  width: 100%;
  height: 47px;
  display: flex;
  align-items: center;
  background-color: rgb(247, 249, 250);
  border-radius: 16px;
  border-bottom: 1px solid #EBEEF0;
}
.trends-for-you {
  font-size: 19px;
  line-height: 25px;
  font-weight: 800;
  padding-left: 15px;
  padding-right: 15px;
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
