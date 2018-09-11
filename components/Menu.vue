<template>
    <div id="nav">
        <div class="brand">
            <h3>simple>Blog</h3>
        </div>
        <div class="middle-nav">
            <Search/>
        </div>
        <div class="right-nav">
            <nuxt-link to="/">&lt;Home/&gt;</nuxt-link>
            <nuxt-link to="/posts">&lt;Posts/&gt;</nuxt-link>
            <nuxt-link to="/newPost">&lt;New Post/&gt;</nuxt-link>
            <nuxt-link to="/about">&lt;About/&gt;</nuxt-link>
        </div>
    </div>
</template>

<script>
import Search from './Search'
export default {
    components: {
        Search
    }
}
</script>

<style>
    #nav {
        grid-column-start: 1;
        grid-column-end: -1;
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-template-rows: 3rem;
    }

    .brand {
        grid-column-start: 1;
        grid-column-end: 3;
        text-align: center;
        align-self: center;
        padding: 0;
        font-family: 'Righteous', cursive;
    }

    .brand h3 {
        margin: 0;
        padding: 0;
        font-size: 2rem;
        color: #181818;
    }

    .middle-nav {
        grid-column-start: 4;
        grid-column-end: 9;
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-template-rows: repeat(12, 1fr);
    }

    .right-nav {
        grid-column-start: 10;
        grid-column-end: -1;
        align-self: center;
        justify-self: center;
    }

    .right-nav a {
        text-decoration: none;
        padding: .13rem;
        margin: .13rem .25rem .13rem .25rem;
        color: #181818;
    }
</style>


