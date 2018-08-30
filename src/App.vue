<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light">
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link to="/" class="nav-link">Home</router-link>
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

<style>
  body {
    max-width: 720px;
    margin: 0 auto;
    font-family: Serif;
  }
</style>
