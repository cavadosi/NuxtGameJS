<template>
  <header class="sticky top-0 z-10">

    <div class="backdrop-blur md:border-b border-gray-800 text-white">
      <nav class="mx-auto flex w-full items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <NuxtLink to="/">  
            <Icon icon="bxs:game" class="text-green-500 w-20 h-8 transform: hover:text-green-700 hover:cursor-pointer"/>
          </NuxtLink>
          
        </div>
        <div class="hidden lg:flex gap-x-12">
          <NuxtLink to="/" class="text-sm font-semibold leading-6 transform hover:text-green my-link">Home</NuxtLink>
          <NuxtLink to="/games/flappybird" class="text-sm font-semibold leading-6 transform hover:text-green my-link">Games</NuxtLink>
          <NuxtLink to="/about" class="text-sm font-semibold leading-6 transform hover:text-green my-link">Product</NuxtLink>
          
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end text-zinc-500">
          <a href="https://github.com/cavadosi" target="blank">
            <Icon icon="icomoon-free:github" class="w-20 h-8 transform hover:text-white hover:cursor-pointer"  />
          </a>
        </div>
        <div class="flex lg:flex-1 lg:justify-end lg:hidden text-zinc-500">
          <button type="button" class="-m-2.5 -mr-6 inline-flex items-center justify-center rounded-md p-2.5 text-primary" @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Icon icon="uil:bars" class="w-20 h-8 transform hover:text-white hover:cursor-pointer"/>
          </button>
        </div>
        <ClientOnly>
          <Dialog as="div" class="md:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
            <div class="fixed inset-0 z-10" />
            <DialogPanel class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-secondary-950/90 backdrop-blur-sm px-6 py-6">
              <div class="flex items-center justify-between">
                <NuxtLink to="/">  
                  <Icon icon="bxs:game" class="text-green-500 w-20 h-8 transform: hover:text-green-700 hover:cursor-pointer"/>
                </NuxtLink>
                <button type="button" class="-m-2.5 rounded-md p-2.5 text-primary" @click="mobileMenuOpen = false">
                  <span class="sr-only">Close menu</span>
                  <Icon icon="maki:cross" class="w-20 h-8 transform hover:text-white hover:cursor-pointer"/>
                </button>
              </div>
              <div class="mt-6 flex justify-center items-center">
                <div class="divide-gray-500/10">
                  <div class="space-y-4 py-8 text-center">
                    <NuxtLink to="/" class="text-sm font-semibold leading-6 transform hover:text-green my-link">Home</NuxtLink>
                    <NuxtLink to="/games/flappybird" class="text-sm font-semibold leading-6 transform hover:text-green my-link">Games</NuxtLink>
                    <NuxtLink to="/about" class="text-sm font-semibold leading-6 transform hover:text-green my-link">Product</NuxtLink>
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

<style scoped>
.my-link.router-link-exact-active {
	@apply text-green-500 font-bold;
}
</style>