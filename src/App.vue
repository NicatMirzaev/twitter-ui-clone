<template>
  <div class="container">
    <Sidebar/>
    <Feed/>
    <Widgets/>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar';
import Feed from './components/Feed';
import Widgets from './components/Widgets.vue';

export default {
  name: 'App',
  components: { Sidebar, Feed, Widgets }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  border: 0;
  font: inherit;
}

html {
  box-sizing: border-box;
  font-size: 15px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
}

body {
  font-size: 1rem;
}

.container {
  display: flex;
  max-width: 1400px;
  margin-right: auto;
  margin-left: auto;
}
</style>
