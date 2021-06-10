<template>
  <div class="bg-gray-900">
    <div class="flex flex-wrap gap-8">
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
