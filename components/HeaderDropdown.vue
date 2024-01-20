<template>
    <Menu as="div" class="relative inline-block text-left">
      <div>
        <MenuButton class="inline-flex w-full justify-center gap-x-1.5 rounded-md px-3  text-sm font-semibold text-white shadow-sm hover:text-primary-700 my-link">
          Games
          <Icon icon="mingcute:down-line" class="-ml-1 mt-0.5 h-5 w-5 text-zinc-500 " aria-hidden="true" />
        </MenuButton>
      </div>

      <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
        <MenuItems class="absolute right-0 z-20 mt-2 w-32 origin-top-right rounded-md md:bg-nuxtGray/50 ring-1 ring-gray-800 shadow-lg focus:outline-none overflow-hidden">
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
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/games/flappyBird',
        isRight: false,
    },
    {
        id: 2,
        name: 'Blackjack',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: true,
    },
    {
        id: 3,
        name: 'Batalla naval',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: false,
    },
    {
        id: 4,
        name: 'Pac-man',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: true,
    },
    {
        id: 5,
        name: 'Tetris',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: false,
    },
    {
        id: 6,
        name: 'Juego Clase',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: true,
    },
];
</script>

<style scoped>
.my-link.router-link-exact-active {
	@apply text-green-500 font-bold;
}

</style>