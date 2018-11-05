<template>
  <ul class="navbar">
    <li><router-link
      class="navbar__item"
      to="/login">Login</router-link></li>
    <li><router-link
      class="navbar__item"
      to="/signup">Sign Up</router-link></li>
  </ul>
</template>

<script>
export default {
  name: 'MainNavbar'
}
</script>

<style lang="scss" scoped>
.navbar {
  display: flex;
  width: 100vw;
  justify-content: flex-end;
  margin-top: 1.2rem;
}

.navbar__item {
  display: block;
  text-align: center;
  font-size: 1.6rem;
  font-family: 'Noto Sans KR', sans-serif;
  border-bottom: solid 1px;
  color: white;
  outline: none;
  text-decoration: none;
  margin-right: 2rem;
  width: 7rem;
  height: 2.4rem;
}
</style>
