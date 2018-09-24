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
      <div class="list-container" v-for="(post, index) in posts" v-bind:key="index">
        <a href="/posts" v-bind="id">
          <div id="most-recent-list" class="most-recent-post">
            <h3>{{ post[0].title }}</h3>
            <p>{{ post[0].description }}</p>
            <p><small>By: {{ post[0].author }}</small></p>
          </div>
        </a>
      </div>
    </div>
    <div id="most-popular-container">
      <h2>Our Popular Posts</h2>
      <div class="list-container">
        <ul id="most-popular-list" v-for="(post, index) in posts" :key="index">
          <li><h3>{{ post[1].title }}</h3>
            <ul>
              <li>{{ post[1].description }}</li>
              <li>By: {{ post[1].author }}</li>
            </ul>
          </li>
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
    padding: 1rem;
  }

</style>

