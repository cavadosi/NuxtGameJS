<template>
  <GameLayout :game="game">

  </GameLayout>
</template>

<script setup>
const game = 
    {
        name: 'Black',
        name2: 'jack',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        textcolor: 'text-lime-600',
        ringcolor: 'ring-lime-600',
        bordercolor: 'border-lime-600',
        shadowcolor: 'shadow-[10px_10px_0px_0px_#65a30d]'
    }
</script>