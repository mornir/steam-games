<template>
  <div class="px-8 py-12 bg-gray-900">
    <div class="c-grid">
      <GameCard v-for="game in games" :key="game.appid" :game="game" />
    </div>
  </div>
</template>

<script>
import games from "./games.json"
import GameCard from "./components/GameCard.vue"

export default {
  components: {
    GameCard,
  },
  data() {
    return {
      games: games,
    }
  },
}
</script>

<style scoped>
.c-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(150px, 100%), 1fr));
  justify-items: center;
  column-gap: 1.5rem;
  row-gap: 0.5rem;
}
</style>
