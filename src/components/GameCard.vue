<template>
  <div
    class="relative overflow-hidden duration-200 ease-in-out cursor-pointer hover:transform hover:scale-105 group"
  >
    <img
      :src="`https://steamcdn-a.akamaihd.net/steam/apps/${game.appid}/library_600x900.jpg`"
      width="150"
      height="225"
      loading="async"
      class="w-full group-hover:filter group-hover:brightness-105"
      :alt="game.name"
    />
    <div
      class="w-52 h-14 opacity-10 absolute transform bottom-[59%] left-[8%] rotate-[35deg] duration-500 origin-top-right group-hover:scale-y-200 group-hover:opacity-20 bg-gradient-to-b from-transparent to-white filter blur-sm"
    ></div>
    <p
      class="relative py-0.5 mx-8 text-xs font-semibold text-center text-white bg-gray-700 rounded-md bottom-4"
    >
      {{ getPlayTime(game.playtime_forever) }}
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
  methods: {
    getPlayTime(minutes) {
      if (minutes >= 120) {
        return (minutes / 60).toFixed(1) + " hours"
      } else {
        return minutes + " minutes"
      }
    },
  },
}
</script>
