<script setup>
import { RouterLink, RouterView } from 'vue-router'

// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <nav class="nav">
      <div class="navLogo">
        <RouterLink to="/" class="logo"></RouterLink>
      </div>
      <div class="navLink">
        <RouterLink to="/"
          >首頁
          <svg viewBox="0 0 20 20" fill="#ccc" xmlns="http://www.w3.org/2000/svg" width="15" height="15">
            <path d="M7.293 4.707 14.586 12l-7.293 7.293 1.414 1.414L17.414 12 8.707 3.293 7.293 4.707z" />
          </svg>
        </RouterLink>
        <RouterLink to="/Bus-Dynamics"
          >公車動態<svg viewBox="0 0 20 20" fill="#ccc" xmlns="http://www.w3.org/2000/svg" width="15" height="15">
            <path d="M7.293 4.707 14.586 12l-7.293 7.293 1.414 1.414L17.414 12 8.707 3.293 7.293 4.707z" /></svg
        ></RouterLink>
        <RouterLink to="/Bus-FAQ"
          >常見問題<svg viewBox="0 0 20 20" fill="#ccc" xmlns="http://www.w3.org/2000/svg" width="15" height="15">
            <path d="M7.293 4.707 14.586 12l-7.293 7.293 1.414 1.414L17.414 12 8.707 3.293 7.293 4.707z" /></svg
        ></RouterLink>
      </div>
    </nav>
  </header>

  <RouterView />
</template>

<style lang="scss">
header {
  width: 100%;
  border: 1px solid blue;
}

nav {
  max-width: 1320px;
  margin: 0 auto;
  border: 1px solid red;
  display: flex;
  height: 110px;
  align-items: center;
  justify-content: space-between;

  .navLogo {
    width: 20%;

    .logo {
      display: block;
      background-repeat: no-repeat;
      background-image: url(/img/logo.svg);
      background-size: contain;
      width: 100%;
      height: 45px;
    }
  }

  .navLink {
    width: 20%;
    display: flex;
    justify-content: space-between;

    a {
      font-weight: bold;
      color: #ccc;
      position: relative;
      font-size: 18px;
    }
  }

  &.fixed {
    width: 100%;
    top: 0;
    position: fixed;
    height: 80px;
    background-color: rgba(2, 11, 18, 0.8);
  }
}
</style>
