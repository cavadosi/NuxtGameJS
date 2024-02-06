<template>
  <section class="sticky top-0 z-30">
    <div
      class="flex sticky top-0 z-40 items-center justify-center bg-nuxtGray text-white mb-20"
    >
      <h1 class="text-4xl md:text-7xl font-bold pb-6 pt-4 text-primary">
        Game Galery
      </h1>
      <div class="hidden md:flex blob mx-8 rounded-full"></div>
    </div>
    <div class="flex items-center justify-center">
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 max-w-5xl gap-x-8 p-5 mb-10 mx-6 text-white"
      >
        <div
          v-for="(game, index) in games"
          :key="index"
          :class="game.ringcolor"
          class="flex-col group/item max-w-72 hover:scale-105 duration-500 ring-4 ring-gray-800 rounded-lg overflow-hidden shadow-xl mb-10"
        >
          <img
            :src="game.image"
            alt="Game Image"
            class="w-full md:w-72 h-60 object-cover object-top md:object-center"
          />
          <div
            class="flex flex-row items-center justify-between md:justify-center p-4 max-h-16 md:p-6 w-full text-white bg-secondary"
          >
            <h2
              class="text-xl font-semibold py-2 mx-4 transform transition-all md:group-hover/item:-translate-x-16 delay-150 duration-250"
            >
              {{ game.name }}
            </h2>
            <NuxtLink :to="game.href">
              <Icon
                icon="memory:play"
                :class="[
                  game.iconcolor,
                  'h-10 w-20 rounded-full -mr-6 md:-mr-20  hover:cursor-pointer md:opacity-0 md:group-hover/item:block transition-all md:group-hover/item:opacity-100 delay-100 duration-400',
                ]"
              />
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
v
<script setup>
import { Icon } from "@iconify/vue";

</script>

<style scoped>
section {
  background-color: #060b23;
  background-image: url(/game-galery.png);
}

.blob {
  width: 80px;
  aspect-ratio: 1;
  border: 10px solid #000;
  background: radial-gradient(farthest-side, #000 98%, #0000) top,
    radial-gradient(farthest-side, #fff700 98%, #0000) top,
    radial-gradient(farthest-side, #0000ff 98%, #0000) left,
    radial-gradient(farthest-side, #ff0000 98%, #0000) right,
    radial-gradient(farthest-side, #00ff00 98%, #0000) bottom, #000;
  background-size: 20px 20px;
  background-repeat: no-repeat;
  filter: blur(4px) contrast(10);
  animation: b 2s infinite;
}
@keyframes b {
  0% {
    background-position: top, top, left, right, bottom;
  }
  25% {
    background-position: right, top, left, right, bottom;
  }
  50% {
    background-position: bottom, top, left, right, bottom;
  }
  75% {
    background-position: left, top, left, right, bottom;
  }
  100% {
    background-position: top, top, left, right, bottom;
  }
}
</style>
