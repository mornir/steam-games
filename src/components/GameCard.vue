<template>
  <div
    class="relative overflow-hidden duration-200 ease-in-out cursor-pointer hover:transform hover:scale-105 group"
  >
    <img
      :src="`https://steamcdn-a.akamaihd.net/steam/apps/${game.appid}/library_600x900.jpg`"
      width="150"
      height="225"
      loading="async"
      :alt="game.name"
    />
    <div
      class="w-52 h-14 bg-white opacity-50 absolute transform bottom-[59%] left-[8%] rotate-[35deg] duration-500 origin-top-right group-hover:scale-y-200"
    ></div>
    <p
      class="relative mx-6 text-center text-white bg-gray-700 rounded-md bottom-4"
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
