<template>
  <div class="login">
    <div class="wrapper">
      <h1 class="login__title">Login</h1>
      <button type="button" class="button button--black">{{ hasExtension ? '확장프로그램으로 로그인' : '확장프로그램 설치하기'}}</button>
      <button type="button" class="button">회원가입</button>
    </div>
    </div>
</template>

<script>
export default {
  data: () => ({
    hasExtension: false
  }),
  created () {
    window.chrome.runtime.sendMessage('aaneldlghmofccpgegijnfaekencbdjn', { message: 'check' }, (reply) => {
      if (reply) this.hasExtension = true
    })

    window.addEventListener('message', e => {
      console.log(e.data)
    })
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  margin: 20vh 0 0 13vw;
}

.login {
  background: center / cover url('../assets/home-background.png');
  height: 100vh;
  width: 100vw;
  overflow: hidden;
}

.login__title {
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 4rem;
  font-weight: bold;
  margin-bottom: 7rem;
}

.button {
  display: block;
  color: black;
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 1.5rem;
  border-radius: 3rem;
  padding: 0.75rem 0rem;
  border: solid 1px;
  background-color: white;
  cursor: pointer;
  margin-bottom: 1.5rem;
  width: 30rem;
}

.button--black {
  background-color: black;
  color: white;
  padding: 1rem 0rem;
}
</style>
