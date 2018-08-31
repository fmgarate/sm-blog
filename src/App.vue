<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light">
      <button class="navbar-toggler" type="button" aria-label="Toggle navigation" v-on:click="showMenu=!showMenu">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" v-bind:class="{show: showMenu}">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link to="/" class="nav-link pl-0">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/about" class="nav-link">About</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/archive" class="nav-link">Archive</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/example-post" class="nav-link">
              Example Post
            </router-link>
          </li>
        </ul>
      </div>
    </nav>
    <div class="container-fluid">
      <router-view/>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        showMenu: false
      }
    }
  }
</script>

<style>
  body {
    max-width: 720px;
    margin: 0 auto;
    font-family: Serif;
  }
</style>
