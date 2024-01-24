<template>
    <Menu as="div" class="relative inline-block text-left">
      <div>
        <MenuButton class="inline-flex w-full justify-center gap-x-1.5 rounded-md px-3  text-sm font-semibold text-white shadow-sm hover:text-primary-700 my-link">
          Games
          <Icon icon="mingcute:down-line" class="-ml-1 mt-0.5 h-5 w-5 text-zinc-500 " aria-hidden="true" />
        </MenuButton>
      </div>

      <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
        <MenuItems class="absolute  md:right-0  z-20 mt-2 w-32 md:origin-top-right rounded-md bg-nuxtGray/50 ring-1 ring-gray-800 shadow-lg focus:outline-none overflow-hidden">
            <MenuItem v-for="(juego, index) in juegos" :key="index" v-slot="{ active }">
              <a :href="juego.href" :class="[active ? 'bg-nuxtGray/70 text-primary-700' : 'text-white', 'block px-4 py-2 text-sm my-link ']">{{ juego.name }}</a>
            </MenuItem>
        </MenuItems>
      </transition>
    </Menu>
  </template>

<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue';
import { Icon } from '@iconify/vue';

const juegos = [
    {
        id: 1,
        name: 'Flappybird',
        href:'/games/flappyBird',
    },
    {
        id: 2,
        name: 'Blackjack',
        href:'/games/blackjack',
    },
    {
        id: 3,
        name: 'Naval Battle',
        href:'/games/naval-battle',
    },
    {
        id: 4,
        name: 'Pac-man',
        href:'/games/pac-man',
    },
    {
        id: 5,
        name: 'Tetris',
        href:'/games/tetris',
    },
    {
        id: 6,
        name: 'Juego Clase',
        href:'/games/juego-clase',
    },
];
</script>

<style scoped>
.my-link.router-link-exact-active {
	@apply text-green-500 font-bold;
}

</style>