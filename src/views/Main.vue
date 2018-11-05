<template>
  <div class="main">
    <div class="main__wrapper">
      <div class="nav">
        <div class="nav__top">
          <img class="nav__logo" src="../assets/main-moon.png">
          <h2 class="nav__title">포문(砲門)</h2>
          <p class="nav__pg">새로운 건전한 스포츠 문화의 포문(砲門)을 열다.</p>
        </div>
        <ul class="nav__items">
          <li class="nav__item-wrapper">
            <router-link
              class="nav__item"
              to="/betting">예측 하러가기</router-link>
          </li>
          <li class="nav__item-wrapper">
            <router-link
              class="nav__item"
              to="/">커뮤니티 이동하기</router-link>
          </li>
          <li class="nav__item-wrapper">
            <router-link
              class="nav__item"
              to="/">금주의 경기 보러가기</router-link>
          </li>
          <li class="nav__item-wrapper">
            <router-link
              class="nav__item"
              to="/">불법 도박사이트 신고하기</router-link>
          </li>
        </ul>
      </div>
      <div class="info">
        <div class="auth">
          <router-link
            class="auth__button"
            to="/login">Login</router-link>
          <router-link
            class="auth__button"
            to="/signup">Sign Up</router-link>
        </div>
        <div class="info__wrapper">
          <this-week/>
          <lose-exp/>
          <live-status/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ThisWeek from '@/components/ThisWeek.vue'
import LoseExp from '@/components/LoseExp.vue'
import LiveStatus from '@/components/LiveStatus.vue'

export default {
  name: 'Main',
  components: { ThisWeek, LoseExp, LiveStatus }
}
</script>

<style lang="scss" scoped>
.main {
  background: left / cover url('../assets/main-background.png');
  width: 100vw;
  height: 100vh;
}

.main__wrapper {
  display: flex;
  height: 100%;
}

.nav {
  width: 30%;
  padding-left: 2.5rem;
  font-family: 'Noto Sans KR', sans-serif;
  color: white;
  overflow: hidden;
}

.nav__top {
  display: flex;
  flex-direction: column;
  margin-bottom: 2rem;
  width: 50%;
}

.nav__logo {
  width: 10rem;
  margin: auto;
  margin-bottom: 1rem;
}

.nav__title {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.nav__pg {
  font-size: 1rem;
  line-height: 1.25;
}

.nav__items {
  font-size: 1.5rem;
}

.nav__item-wrapper {
  margin: 5rem 1rem;
}

.nav__item {
  color: white;
  text-decoration: none;
  cursor: pointer;
}

.info {
  display: flex;
  flex-direction: column;
  width: 60%;
}

.auth {
  display: flex;
  width: 108%;
  justify-content: flex-end;
  padding: 1rem 0;
}

.auth__button {
  color: black;
  text-decoration: none;
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 1.5rem;
  margin-right: 1rem;
  border-radius: 3rem;
  height: 2rem;
  padding: 0.725rem 2rem;
  border: solid 1px;
  background-color: white;
  vertical-align: middle;
  cursor: pointer;
}

.info__wrapper {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  margin-top: 1rem;
}

.info__wrapper > * {
  margin: 1rem;
  width: 50%;
  flex-shrink: 1;
  flex: 0 1;

}
</style>
