<template>
  <div id="grid-wrapper">
    <div id="menu-wrapper">
      <Menu/>
    </div>
    <div id="content-wrapper">
      <nuxt/>
    </div>
  </div>
</template>

<script>
import Menu from '../components/Menu.vue'
import json from '~/static/posts.json'
export default {
  data() {
    return {
      posts: json
    }
  },
  components: {
    Menu
  }
  
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Raleway|Righteous');
  /*
  *  font-family: 'Raleway', sans-serif;
  *  font-family: 'Righteous', cursive;
  */

  html {
    background-color: #3a6db0;
    background-image: url("data:image/svg+xml,%3Csvg width='84' height='48' viewBox='0 0 84 48' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M0 0h12v6H0V0zm28 8h12v6H28V8zm14-8h12v6H42V0zm14 0h12v6H56V0zm0 8h12v6H56V8zM42 8h12v6H42V8zm0 16h12v6H42v-6zm14-8h12v6H56v-6zm14 0h12v6H70v-6zm0-16h12v6H70V0zM28 32h12v6H28v-6zM14 16h12v6H14v-6zM0 24h12v6H0v-6zm0 8h12v6H0v-6zm14 0h12v6H14v-6zm14 8h12v6H28v-6zm-14 0h12v6H14v-6zm28 0h12v6H42v-6zm14-8h12v6H56v-6zm0-8h12v6H56v-6zm14 8h12v6H70v-6zm0 8h12v6H70v-6zM14 24h12v6H14v-6zm14-8h12v6H28v-6zM14 8h12v6H14V8zM0 8h12v6H0V8z' fill='%235096b6' fill-opacity='0.4' fill-rule='evenodd'/%3E%3C/svg%3E");
    font-size: 12pt;
    font-family: 'Raleway', sans-serif;
  }

  #grid-wrapper {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 3.25rem repeat(11, 1fr);
  }

  #menu-wrapper {
    grid-column-start: 1;
    grid-column-end: -1;
    grid-row-start: 1;
    grid-row-end: 1;
    display: grid;
    height: 3rem;
    background-color: #d9d9d9;
    border-radius: 1rem;
    margin: 0;
    padding: 0;
    grid-template-columns: repeat(12, 1fr);
  }

  #content-wrapper {
    grid-column-start: 1;
    grid-column-end: -1;
    grid-row-start: 2;
    grid-row-end: 10;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(12, 1fr);
  }
</style>