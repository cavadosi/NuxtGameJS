<template>
  <GameLayout :game="game">
    <div class="flex items-center justify-center size-full">
      <h1 class="mx-4">Work in progress</h1>
    </div>
  </GameLayout>
</template>

<script setup>
const game = {
  name: "Naval ",
  name2: "battle",
  description:
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
  textcolor: "text-sky-400",
  ringcolor: "ring-sky-400",
  bordercolor: "border-sky-400",
  shadowcolor: "shadow-[10px_10px_0px_0px_#38bdf8]",
};
</script>
