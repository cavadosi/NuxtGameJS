<template>
  <section class="sticky top-0 z-30">
    <div class="flex sticky top-0 z-40 items-center justify-center   bg-nuxtGray text-white mb-20"> 
      <h1 class="text-xxl md:text-7xl font-bold pb-6 pt-4 text-primary ">Game Galery</h1>
      <div class="hidden md:flex blob mx-8 rounded-full"></div>
    </div>
    <div class="max-w-5xl p-5 mb-10 mx-6 text-white">
      <div v-for="(game, index) in games" :key="index" class="transform transition-transform hover:scale-105 bg-secondary-900 ring-2 ring-gray-800 hover:ring-primary rounded-lg overflow-hidden shadow-xl mb-10">
        <div :class="{ 'md:flex-row-reverse': game.isRight }" class="md:flex md:flex-row">
          <img :src="game.img" alt="Game Image" class="w-full md:w-96 h-64 object-cover object-top md:object-center" />
          <div class="p-6 md:p-8 w-full text-white">
            <h2 class="text-lg font-bold mb-4 mx-4">{{ game.name }}</h2>
            <p class="max-w-sm">{{ game.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>



<script setup>

const props = defineProps({
	games: {
		type: Object,
		required: true
	}
});

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
  background: 
    radial-gradient(farthest-side,#000 98%,#0000) top,
    radial-gradient(farthest-side,#fff700 98%,#0000) top,
    radial-gradient(farthest-side,#0000FF 98%,#0000) left,
    radial-gradient(farthest-side,#FF0000 98%,#0000) right,
    radial-gradient(farthest-side,#00FF00 98%,#0000) bottom,
    #000;
  background-size:20px 20px;
  background-repeat: no-repeat;
  filter: blur(4px) contrast(10); 
  animation: b 2s infinite;
}
@keyframes b {
  0%   {background-position:top,top,left,right,bottom}
  25%  {background-position:right,top,left,right,bottom}
  50%  {background-position:bottom,top,left,right,bottom}
  75%  {background-position:left,top,left,right,bottom}
  100% {background-position:top,top,left,right,bottom}
}

</style>