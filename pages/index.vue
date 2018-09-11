<template>
  <div id="content-home">
    <ul v-for="(post, index) in posts" :key="index">
      <li>{{ post.title }}</li>
    </ul>
  </div>  
</template>

<script>
import json from '~/static/posts.json'
export default {
  data() {
        return {
          posts: json
        }
    }
}
</script>

<style>
  #content-home {
    background-color: rgba(54, 54, 54, .85);
    height: 100rem;
    grid-column-start: 1;
    grid-column-end: -1;
    grid-row-start: 1;
    grid-row-end: -1;
    border-radius: 2rem;
  }

</style>

