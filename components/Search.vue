<template>
    <div class="search-container">
        <form class="search-form" method="post">
            <input type="text" class="search-input" name="search" placeholder="Search">
            <button class="search-btn">Go</button>
        </form>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .search-container {
        grid-column-start: 1;
        grid-column-end: -1;
        grid-row-start: 1;
        grid-row-end: 1;
        justify-self: center;
        padding-top: .4rem;
    }
    .search-form {
        width: 100%;
    }

    .search-input {
        width: 38rem;
        height: 2rem;
        font-size: 1.25rem;
        box-shadow: none;
        border: none;
        border-radius: 1rem;
        padding-left: .5rem;
        background-color: #e6e6e6;
    }

    .search-input:focus {
        border-radius: .5rem;
        background-color: white;
        outline: none;
        font-weight: lighter;
    }

    .search-btn {
        height: 2rem;
        width: 3rem;
        border-radius: 0 1rem 1rem 0;
        box-shadow: 0;
        border: none;
        background-color: rgba(0, 0, 0, 0);
        font-size: 1rem;
        cursor: pointer;
    }

</style>

