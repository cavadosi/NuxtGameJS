<template>
    <Menu as="div" class="relative inline-block text-left">
      <div>
        <MenuButton class="inline-flex w-full justify-center gap-x-1.5 rounded-md px-3  text-sm font-semibold text-white shadow-sm hover:text-primary-700 my-link">
          Games
          <Icon icon="mingcute:down-line" class="-mr-1 h-5 w-5 text-zinc-500" aria-hidden="true" />
        </MenuButton>
      </div>

      <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
        <MenuItems class="absolute right-0 mt-2 w-32 origin-top-right rounded-md bg-nuxtGray shadow-lg focus:outline-none">
          <div >
            <MenuItem v-slot="{ active }">
              <a href="/games/flappybird" :class="[active ? 'bg-secondary text-primary-700' : 'text-white', 'block px-4 py-2 text-sm my-link']">FlappyBird</a>
            </MenuItem>
            <MenuItem v-slot="{ active }">
              <a href="#" :class="[active ? 'bg-secondary text-primary-700' : 'text-white', 'block px-4 py-2 text-sm my-link']">Blackjack</a>
            </MenuItem>
            <MenuItem v-slot="{ active }">
              <a href="#" :class="[active ? 'bg-secondary text-primary-700' : 'text-white', 'block px-4 py-2 text-sm my-link']">Juego Clases</a>
            </MenuItem>
            
          </div>
        </MenuItems>
      </transition>
    </Menu>
  </template>

<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue';
import { Icon } from '@iconify/vue';

</script>

<script>

export default {
components: {
    Icon,
},
};

</script>

<style scoped>
.my-link.router-link-exact-active {
	@apply text-green-500 font-bold;
}

</style>