<template>
  <div class="container">
    <Sidebar/>
    <Feed/>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar';
import Feed from './components/Feed';

export default {
  name: 'App',
  components: { Sidebar, Feed }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  border: 0;
  font: inherit;

  *,
  *:before, *: after {
    box-sizing: inherit;
  }
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
  max-width: 1300px;
  margin-right: auto;
  margin-left: auto;
}
</style>
