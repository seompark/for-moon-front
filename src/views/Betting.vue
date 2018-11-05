<template>
  <div class="bet">
    <div class="navbar">
      <div class="navbar__brand" @click="$router.push('/')">
        <img class="navbar__brand-img" src="../assets/main-moon.png">
      </div>
      <div class="navbar__left">
        <router-link
              class="navbar__button"
              to="/login">Login</router-link>
            <router-link
              class="navbar__button"
              to="/signup">Sign Up</router-link>
      </div>
    </div>
    <div class="bet__content">
      <div class="bet__interface">
        <img class="bet__image" src="../assets/bet.png">
      </div>
      <div class="bet__3rd">
        <div class="bet__yt-wrapper">
          <iframe src="https://www.youtube.com/embed/vMbbDpPZ6Fs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="bet__yt-chat">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Betting'
}
</script>

<style lang="scss" scoped>
.bet {
  height: 100vh;
}

.navbar {
  display: flex;
  align-items: center;
  background-color: black;
  padding: 0.725rem 0;
  height: 5.5rem;
}

.navbar__brand {
  margin-left: 1.2rem;
  margin-bottom: 0.3rem;
}

.navbar__brand-img {
  width: 6rem;
  cursor: pointer;
}

.navbar__left {
  flex: 0 1;
  margin-left: auto;
  display: flex;
}

.navbar__button {
  color: white;
  text-decoration: none;
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 1.5rem;
  margin-right: 1rem;
  border-radius: 3rem;
  width: 5.5rem;
  text-align: center;
  padding: 1rem 2rem;
  border: solid 1px white;
  vertical-align: middle;
  cursor: pointer;
}

.bet__content {
  display: flex;
  height: calc(100vh - 6rem);
  margin: 4rem 0;
}

.bet__interface {
  width: 50%;
}

.bet__image {
  width: 100%;
}

.bet__3rd {
  width: 50%;
}

.bet__yt-wrapper {
  position: relative;
  padding: 25px 0 56.25% 0;
  height: 0;
}

.bet__yt-wrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
