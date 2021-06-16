<template>
  <div class=" navbar navbar-dark navbar-expand-lg bg-primary">
    <div class="container">
      <div class="navbar-brand">
        Vue.js
      </div>
      <div class="collapse navbar-collapse" id="navbarText">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item ">
             <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about">About</router-link>
          </li>
        
        </ul>
      </div>
      
    </div>
  </div>
  <div class="p-5">
    <router-view />
  </div>
</template>

<script></script>

<style></style>
