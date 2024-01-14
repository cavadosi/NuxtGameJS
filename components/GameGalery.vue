<template>
    <div class="flex items-center justify-center max-h-full border-y border-gray-800 text-white mb-20"> 
        <h1 class="text-4xl md:text-7xl font-bold p-10 ">Game Galery</h1>
    </div>
    <div class="max-w-5xl p-5 mb-10 mx-6 text-white">
        <div v-for="game in games" :key="games.id" class="transform transition-transform hover:scale-105 bg-secondary-900 ring-2 ring-gray-800 hover:ring-green-500 rounded-lg overflow-hidden shadow-xl mb-10">
            <div :class="{ 'md:flex-row-reverse': game.isRight }" class="md:flex md:flex-row">
                <img :src="game.img" alt="Game Image" class="w-full md:w-96 h-64 object-cover object-top md:object-center" />
                <div class="p-6 md:p-8 w-full text-white">
                    <h2 class="text-lg font-bold mb-4 mx-4">{{ game.name }}</h2>
                    <p class="max-w-sm">{{ game.description }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

const props = defineProps({
	games: {
		type: Object,
		required: true
	}
});



</script>