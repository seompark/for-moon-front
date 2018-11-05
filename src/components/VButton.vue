<template>
  <button class="button" @click="e => emit('click', e)"><slot/></button>
</template>

<script>
export default {
  name: 'VButton'
}
</script>

<style lang="scss" scoped>
.button {
  color: black;
  text-decoration: none;
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 1rem;
  border-radius: 3rem;
  padding: 0.4rem 2.2rem;
  border: solid 1px;
  background-color: white;
  cursor: pointer;
}
</style>
