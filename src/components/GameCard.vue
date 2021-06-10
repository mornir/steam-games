<template>
  <div
    class="
      cursor-pointer
      hover:transform
      hover:scale-105
      duration-200
      ease-in-out
    "
  >
    <img
      :src="`https://steamcdn-a.akamaihd.net/steam/apps/${game.appid}/library_600x900.jpg`"
      width="150"
      height="225"
      loading="async"
      :alt="game.name"
    />
    <p
      class="
        text-white
        bg-gray-700
        text-center
        mx-6
        relative
        bottom-4
        rounded-md
      "
    >
      14.3 hours
    </p>
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
