<template>
    <div class="flex-col justify-center">
        <div class="flex flex-col md:flex-row items-center justify-center max-w-full py-10 md:py-24 md:pb-40 md:gap-x-16 lg:gap-x-28">
            <div class="flex flex-col items-center justify-center text-white mb-8 md:mb-16">
                <h1 class="text-3xl lg:text-5xl mb-5 lg:mb-10">Welcome to</h1>
                <h2 class="text-5xl lg:text-7xl text-green-500 font-medium">My JS games</h2>
            </div>
            <div class="flex items-end justify-center p-10">
                <GameSlider class="overflow-clip"/>
            </div>
        </div>
        
        <GameGalery :games="juegos" />
    </div>
</template> 


<script setup>


const juegos = [
    {
        id: 1,
        name: 'Flappy bird',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: false,
    },
    {
        id: 2,
        name: 'Flappy bird',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: true,
    },
    {
        id: 3,
        name: 'Flappy bird',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: false,
    },
    {
        id: 4,
        name: 'Flappy bird',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: true,
    },
    {
        id: 5,
        name: 'Flappy bird',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: false,
    },
    {
        id: 6,
        name: 'Flappy bird',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/flappyBird',
        isRight: true,
    },
];

</script>