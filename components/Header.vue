<template>
  <header class="sticky top-0 z-10">

    <div class="backdrop-blur md:border-b border-gray-800 text-white">
      <nav class="mx-auto flex w-full items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex md:flex-1">
          <NuxtLink to="/">  
            <Icon icon="bxs:game" class="text-primary w-8 md:w-20 h-8 transform: hover:text-primary-700 hover:cursor-pointer"/>
          </NuxtLink>
          
        </div>
        <div class="hidden md:flex gap-x-12">
          <NuxtLink to="/" class="text-sm font-semibold leading-6 transform hover:text-primary-700 my-link">Home</NuxtLink>
          <HeaderDropdown />
          <NuxtLink to="/about" class="text-sm font-semibold leading-6 transform hover:text-primary-700 my-link">About</NuxtLink>
          
        </div>
        <div class="hidden md:flex md:flex-1 md:justify-end rounded-full text-zinc-500">
          <a href="https://github.com/cavadosi" target="blank">
            <Icon icon="icomoon-free:github" class="w-8 h-8 transform hover:text-white hover:cursor-pointer"  />
          </a>
        </div>
        <div class="flex flex-1 justify-end md:hidden text-zinc-500">
          <button type="button" class="-m-2.5 -mr-6 inline-flex items-center justify-center rounded-md p-2.5 text-primary" @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Icon icon="uil:bars" class="w-8 h-8 transform hover:text-white hover:cursor-pointer"/>
          </button>
        </div>
        <ClientOnly>
          <Dialog as="div" class="md:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
            <div class="fixed inset-0 z-10" />
            <DialogPanel class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-secondary-950/90 backdrop-blur-sm px-6 py-6">
              <div class="flex items-center justify-between">
                <NuxtLink to="/">  
                  <Icon icon="bxs:game" class="text-primary w-20 h-8 transform: hover:text-green-700 hover:cursor-pointer"/>
                </NuxtLink>
                <button type="button" class="-m-2.5 rounded-md p-2.5 text-primary" @click="mobileMenuOpen = false">
                  <span class="sr-only">Close menu</span>
                  <Icon icon="maki:cross" class="w-20 h-8 transform hover:text-white hover:cursor-pointer"/>
                </button>
              </div>
              <div class="mt-6 flex justify-center items-center text-white">
                <div class="divide-gray-500/10">
                  <div class="flex flex-col space-y-4 py-8 text-center">
                    <NuxtLink to="/" class="text-sm font-semibold leading-6 transform hover:text-primary-700 my-link">Home</NuxtLink>
                    <NuxtLink to="/games/flappybird" class="text-sm font-semibold leading-6 transform hover:text-primary-700 my-link">Games</NuxtLink>
                    <NuxtLink to="/about" class="text-sm font-semibold leading-6 transform hover:text-primary-700 my-link">About</NuxtLink>
                  </div>
                </div>
              </div>
            </DialogPanel>
          </Dialog>
        </ClientOnly>
      </nav>
    </div>
  </header>
</template> 

<script >
import { Dialog, DialogPanel } from '@headlessui/vue';

export default {
	components: {
		Icon,
	},
};

</script>

<script setup>
import { Icon } from '@iconify/vue';
const mobileMenuOpen = ref(false);

</script>

<style>
.my-link.router-link-exact-active {
	@apply text-green-500 font-bold;
}
</style>