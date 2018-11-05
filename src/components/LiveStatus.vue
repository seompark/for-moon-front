<template>
  <div class="live">
    <div class="live__card">
      <img class="live__image" src="../assets/main-premier.png">
      <div class="live__wrapper">
        <div class="live__info">
          <span class="live__minutes">전반 42분</span>
          <span class="live__score">1 : 0</span>
        </div>
        <div class="live__teams">맨시티 <span class="live__vs">vs</span> 사우스샘프턴</div>
      </div>
      </div>
    <div class="live__yt">
      <iframe id="ytplayer" type="text/html"
        src="http://www.youtube.com/embed/vMbbDpPZ6Fs?autoplay=1"
        frameborder="0"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LiveStatus'
}
</script>

<style lang="scss" scoped>
.live__card {
  font-family: 'Noto Sans KR', sans-serif;
  display: flex;
  border: 2px solid;
  border-radius: 1rem;
  overflow: hidden;
  align-items: center;
}

.live__minutes {
  color: #909090;
  font-size: 1.25rem;
}

.live__teams {
  font-size: 2.25rem;
  font-weight: bold;
}

.live__score {
  font-size: 2rem;
  font-weight: bold;
}

.live__info {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-bottom: 0.25rem;
}

.live__vs {
  color: #909090;
}

.live__yt {
  margin-top: 2rem;
  position: relative;
  padding: 25px 0 56.25% 0;
  height: 0;
}

.live__yt iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.live__image {
  width: 8rem;
  height: 11rem;
}
</style>
