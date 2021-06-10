<template>
  <div
    class="
      cursor-pointer
      hover:transform
      hover:scale-105
      duration-200
      ease-in-out
      relative
      overflow-hidden
      group
    "
  >
    <img
      :src="`https://steamcdn-a.akamaihd.net/steam/apps/${game.appid}/library_600x900.jpg`"
      width="150"
      height="225"
      loading="async"
      :alt="game.name"
    />
    <div
      class="
        w-44
        h-24
        bg-red-500
        absolute
        top-0
        right-0
        transform
        rotate-45
        origin-bottom-right
        group-hover:bg-green-500
      "
    ></div>
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
