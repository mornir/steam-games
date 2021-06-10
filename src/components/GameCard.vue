<template>
  <div>
    <img
      :src="`https://steamcdn-a.akamaihd.net/steam/apps/${game.appid}/library_600x900.jpg`"
      width="150"
      height="225"
      loading="async"
      :alt="game.name"
    />
  </div>
</template>

<script>
export default {
  props: {
    game: {
      type: Object,
      default: () => {},
      required: true,
    },
  },
}
</script>
