<template>
    <div class="backdrop-blur border-b border-gray-800 text-white sticky top-0 lg:">
        <nav class="mx-auto flex w-full items-center justify-between p-6 lg:px-8" aria-label="Global">
          <div class="flex lg:flex-1">
            <a href="/" target="blank">  
              <Icon icon="bxs:game" class="text-green-500 w-20 h-8 transform: hover:text-green-700 hover:cursor-pointer"/>
            </a>

          </div>
          <div class="flex gap-x-12">
              <a href="#" class="text-sm font-semibold leading-6 transform hover:text-green-500">Product</a>
              <a href="#" class="text-sm font-semibold leading-6 transform hover:text-green-500">Features</a>
              <a href="#" class="text-sm font-semibold leading-6 transform hover:text-green-500">Company</a>
              <a href="#" class="text-sm font-semibold leading-6 transform hover:text-green-500">Marketplace</a>
          </div>
          <div class="hidden lg:flex lg:flex-1 lg:justify-end text-zinc-500">
            <a href="https://github.com/cavadosi" target="blank">
              <Icon icon="icomoon-free:github" class="w-20 h-8 transform hover:text-white hover:cursor-pointer"  />
            </a>
          </div>
        </nav>
    </div>
</template> 

<script>
import { Icon } from '@iconify/vue';

export default {
	components: {
		Icon,
	},
};

</script>