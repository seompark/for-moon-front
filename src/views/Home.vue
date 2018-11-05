<template>
  <div class="home">
    <main-navbar></main-navbar>
    <div class="wrapper">
      <div class="text">
        <h1 class="text__header">포문(砲門) :</h1>
        <p class="text__pg">새로운 건전한 스포츠 문화의 포문(砲門)을 열다.</p>
      </div>
      <router-link
        to="/main"
        class="enter-button">ENTER →</router-link>
    </div>
  </div>
</template>

<script>
import MainNavbar from '@/components/MainNavbar.vue'

export default {
  name: 'home',
  components: {
    MainNavbar
  }
}
</script>

<style lang="scss" scoped>
.home {
  background: center / cover url('../assets/home-background.png');
  height: 100vh;
  width: 100vw;
  overflow: hidden;
}

.wrapper {
  margin: 23vh 0 2rem 5rem;
}

.text {
  font-family: 'Noto Serif KR', serif;
  margin-bottom: 3rem;
}

.text__header {
  font-size: 4.2rem;
  margin-bottom: 1.3rem;
}

.text__pg {
  font-size: 1.5rem;
}

.enter-button {
  color: black;
  text-decoration: none;
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 1rem;
  border-radius: 3rem;
  padding: 1rem 3.2rem;
  border: solid 1px;
  background-color: white;
  cursor: pointer;
}

.enter-button:hover {
  background-color: black;
  border-color: white;
  color: white;
}

.enter-button:focus {
  outline: 0;
}
</style>
