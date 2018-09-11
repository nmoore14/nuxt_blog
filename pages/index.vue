<template>
  <div id="content-home">
    <div id="welcome-container">
      <h2 class="welcome-header">simple>Blog</h2>
      <div class="welcome-text">
        <p>
          Welcome to my simple blog built with VueJS, NuxtJS, Firebase, and others.<br/>
          Feel free to download source code and make it your own.
        </p>
      </div>
    </div>
    <div id="most-recent-container">
      <h2>Most Recent Posts</h2>
      <div class="list-container">
        <ul id="most-recent-list" v-for="(post, index) in posts" :key="index">
          <li>{{ post[0].title }}</li>
        </ul>
      </div>
    </div>
    <div id="most-popular-container">
      <h2>Our Popular Posts</h2>
      <div class="list-container">
        <ul id="most-popular-list" v-for="(post, index) in posts" :key="index">
          <li>{{ post[1].title }}</li>
        </ul>
      </div>
    </div>
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
    grid-column-start: 1;
    grid-column-end: -1;
    grid-row-start: 1;
    grid-row-end: -1;
    border-radius: 2rem;
    padding: 1rem;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(12, 1fr);
    grid-gap: 1rem;
  }

  #welcome-container {
    grid-column-start: 1;
    grid-column-end: -1;
    grid-row-start: 1;
    grid-row-end: 2;
  }

  #welcome-container h2 {
    font-family: 'Righteous', cursive;
    font-size: 4rem;
    color: #d9d9d9;
    text-align: center;
    padding: 0;
    margin: 0;
  }

  #welcome-container p {
    background-color: #d9d9d9;
    color: black;
    text-align: center;
    border-radius: 1rem;
    font-family: 'Raleway', sans-serif;
    font-size: 1.5rem;
    margin: 0;
    padding-top: .5rem;
    padding-bottom: .5rem;
  }

  #most-recent-container {
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 2;
    grid-row-end: -1;
  }

  #most-popular-container {
    grid-column-start: 7;
    grid-column-end: -1;
    grid-row-start: 2;
    grid-row-end: -1;
  }

  #most-recent-container h2, #most-popular-container h2 {
    font-family: 'Righteous', cursive;
    font-size: 3rem;
    color: #d9d9d9;
    text-align: center;
    padding: 0;
    margin: 0;
  }

  .list-container {
    background-color: #d9d9d9;
    color: black;
    font-family: 'Raleway', sans-serif;
    font-size: 1rem;
    border-radius: 1rem;
  }

</style>

