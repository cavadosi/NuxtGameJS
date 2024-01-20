<template>
    <div class="relative">
        <div class="relative">
            <div class="flex-col justify-center">
                <div class="flex flex-col md:flex-row items-center justify-center max-w-full pb-10 md:py-24 md:pb-40 lg:pt-28 lg:pb-56 md:gap-x-16 lg:gap-x-28">
                    <div class="flex flex-col items-center md:items-start text-white m-8 ">
                        <h1 class="text-3xl lg:text-5xl mb-4">Welcome to</h1>
                        <h1 class="text-5xl lg:text-7xl text-primary font-medium">My JS games</h1>
                    </div>
                    <div class="flex items-end justify-center mt-16 mb-20 md:m-10">
                        <GameSlider class="overflow-hidden"/>
                    </div>
                </div>
                
                <div class="custom-shape-divider-bottom absolute bottom-0">
                    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                        <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill-black"></path>
                        <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill-black"></path>
                        <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill-black"></path>
                    </svg>
                </div>
            </div>
        </div>
        <GameGalery :games="juegos" />
        <div class="custom-shape-divider-bottom absolute bottom-0 z-40">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill-green"></path>
                <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill-green"></path>
                <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill-green"></path>
            </svg>
        </div>
    </div>
</template> 

<style scoped>

.custom-shape-divider-bottom {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
    transform: rotate(180deg);
}

.custom-shape-divider-bottom svg {
    position: relative;
    display: block;
    width: calc(100% + 1.3px);
    height: 45px;
}

.custom-shape-divider-bottom .shape-fill-black {
    fill: #060B23;
}

.custom-shape-divider-bottom .shape-fill-green {
    fill: #22c55e;
}

</style>

<script setup>

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
        href:'/games/blackjack',
        isRight: true,
    },
    {
        id: 3,
        name: 'Naval Battle',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/games/naval-battle',
        isRight: false,
    },
    {
        id: 4,
        name: 'Pac-man',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/games/pac-man',
        isRight: true,
    },
    {
        id: 5,
        name: 'Tetris',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/games/tetris',
        isRight: false,
    },
    {
        id: 6,
        name: 'Juego Clase',
        description : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.',
        image: '',
        href:'/games/juego-clase',
        isRight: true,
    },
];

</script>


