<template>
  <div
    class="flex flex-col md:flex-row-reverse items-center justify-center pt-24 -mt-16 max-w-7xl mx-4 lg:mx-16 pb-20"
  >
    <!-- Contenedor del Juego -->

    <div
      class="relative items-center justify-center max-h-full h-[80vh] max-w-[50vh] text-white"
    >
      <slot />
      <div
        :class="[
          game.bordercolor,
          game.shadowcolor,
          'absolute inset-0 -z-10 bg-secondary rounded-md border-2 size-full',
        ]"
      ></div>
    </div>

    <!-- Descripcion del juego -->
    <div
      :class="[
        game.ringcolor,
        'relative items-start bg-nuxtGray -z-10 text-white max-h-full md:rounded-l-md ring-2 mx-6 md:mx-0 p-8 md:pt-8 h-full max-w-[85vw]  md: w-96',
      ]"
    >
      <div class="flex text-2xl font-bold pb-8">
        <h1>
          {{ game.name }}<span :class="[game.textcolor]">{{ game.name2 }}</span>
        </h1>
      </div>
      <div class="text-sm text-zinc-400 pb-4 pr-10">
        {{ game.description }}
      </div>

      <div
        class="hidden md:block absolute inset-0 inset-x-[2px] -z-10 rounded-l-md bg-nuxtGray h-full w-96"
      ></div>
    </div>
  </div>
</template>
<div :style="styleObject"></div>
<style>
.bg-texture {
  background-color: #060b23;
  background-image: url(/game-galery.png);
}
</style>

<script setup>
const props = defineProps({
  game: {
    type: Object,
    required: true,
  },
});
</script>
