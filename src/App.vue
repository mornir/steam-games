<template>
  <div class="bg-gray-900 py-12 px-8">
    <div class="flex flex-wrap gap-x-8 gap-y-2 justify-between">
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
