<template>
  <div class="loseexp">
    <p>
      이번주 <span class="bold">256명</span>이 <br>
      총 <span class="bold bold--red">85700exp</span>를 잃었습니다.
    </p>
  </div>
</template>

<script>
export default {
  name: 'LoseExp'
}
</script>

<style lang="scss" scoped>
.loseexp {
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 2.25rem;
  display: flex;
  justify-content: center;
  padding: 2rem 1rem;
  border: 2px solid;
  border-radius: 1rem;
}

.bold {
  font-size: 3rem;
  font-weight: bold;
}

.bold--red {
  color: red;
}
</style>
