<template>
  <div class="thisweek">
    <h3 class="thisweek__title">금주의 경기</h3>
    <div class="divider"></div>
    <div class="thisweek__games">
      <div
      class="thisweek__game"
      v-for="(game, index) in games"
      :key="index">
      <div class="thisweek__game-number">
        {{ '0' + (index + 1) }}
      </div>
      <div class="thisweek__game-info">
        <p class="thisweek__game-time">{{ game.date }}</p>
        <p class="thisweek__game-teams">{{ game.teams.join(' vs ') }}</p>
      </div>
    </div>
    </div>
    <div class="divider"></div>
  </div>
</template>

<script>
export default {
  name: 'ThisWeek',
  data: () => ({
    games: [
      {
        teams: ['맨시티', '사우스샘프텀'],
        date: '11.05 (월) / 00:00'
      },
      {
        teams: ['첼시 FC', '크리스탈팰리스'],
        date: '11.05 (월) / 01:00'
      },
      {
        teams: ['허더즈필드 타운', '풀럼'],
        date: '11.05 (월) / 05:00'
      },
      {
        teams: ['비야레얄 FC', '레반테 UD'],
        date: '11.06 (화) / 00:15'
      },
      {
        teams: ['레알 소시에다드', '세비야 FC'],
        date: '11.05 (월) / 02:30'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
.thisweek {
  font-family: 'Noto Sans KR', sans-serif;
  margin-bottom: 2rem;
}

.thisweek__title {
  font-size: 3.5rem;
  margin-bottom: 1.5rem;
  font-weight: bold;
}

.thisweek__game {
  display: flex;
  align-items: center;
  padding-bottom: 1rem;
}

.thisweek__game:first-child {
  margin-top: 1rem;
}

.thisweek__game:not(:last-child) {
  border-bottom: 1px solid #707070;
  margin-bottom: 1rem;
}

.thisweek__game-number {
  color: purple;
  float: left;
  font-size: 4rem;
  margin-right: 1rem;
  font-weight: bolder;
}

.thisweek__game-info {

}

.thisweek__game-time {
  color: #303030;
  margin-bottom: 0.5rem;
}

.thisweek__game-teams {
  font-size: 2rem;
  font-weight: bold;
}

.divider {
  border-bottom: 2px solid;
}
</style>
