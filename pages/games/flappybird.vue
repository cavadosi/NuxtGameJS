<template>
  <div
    class="flex-col md:flex md:flex-row-reverse items-center justify-center max-h-screen pt-16 pb-48 max-w-7xl lg:mx-16"
  >
    <!-- Contenedor del Juego -->

    <div
      class="relative items-center justify-center max-w-7xl max-h-full lg:p-72 text-white"
    >
      <div
        class="absolute inset-0 -z-10 bg-secondary shadow-[10px_10px_0px_0px_#22c55e] rounded-md border-2 border-primary size-full"
      ></div>
    </div>

    <!-- Descripcion del juego -->
    <div
      class="relative items-start bg-nuxtGray -z-10 text-white max-h-full rounded-l ring-2 ring-primary px-8 pt-8 h-96 w-96"
    >
      <div class="flex text-2xl font-bold pb-8">
        <h1>Flappy<span class="text-primary">bird</span></h1>
      </div>
      <div class="text-sm text-zinc-400 pr-10">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque,
        consequuntur est excepturi reiciendis facilis fugit soluta ad! Placeat,
        laboriosam voluptas ex possimus veritatis dolorum! Molestiae quas eius
        temporibus cum inventore.
      </div>

      <div
        class="absolute inset-0 inset-x-[2px] -z-10 rounded-l-md bg-nuxtGray h-96 w-96"
      ></div>
    </div>
  </div>
</template>

<style>
.bg-texture {
  background-color: #060b23;
  background-image: url(/game-galery.png);
}
</style>
