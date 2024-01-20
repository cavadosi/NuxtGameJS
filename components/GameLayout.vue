<template>
  <div
    class="flex-col md:flex md:flex-row-reverse items-center justify-center max-h-screen pt-16 pb-48 max-w-7xl lg:mx-16"
  >
    <!-- Contenedor del Juego -->

    <div
      class="relative items-center justify-center max-w-7xl max-h-full lg:p-72 text-white"
    >
      <slot/>
      <div
        :class="[game.bordercolor, game.shadowcolor , 'absolute inset-0 -z-10 bg-secondary rounded-md border-2 size-full']"
      ></div>
    </div>

    <!-- Descripcion del juego -->
    <div
      :class="[game.ringcolor, 'relative items-start bg-nuxtGray -z-10 text-white max-h-full rounded-l ring-2 px-8 pt-8 h-96 w-96']"
    >
      <div class="flex text-2xl font-bold pb-8">
        <h1>{{ game.name }}<span :class="[game.textcolor]">{{ game.name2 }}</span></h1>
      </div>
      <div class="text-sm text-zinc-400 pr-10">
        {{ game.description }}
      </div>

      <div
        class="absolute inset-0 inset-x-[2px] -z-10 rounded-l-md bg-nuxtGray h-96 w-96"
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
		required: true
	}
});


</script>
