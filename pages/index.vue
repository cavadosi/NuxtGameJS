<template>
    <div class="flex-col justify-center">
        <div class="flex flex-col md:flex-row items-center justify-center max-w-full pb-10 md:py-24 md:pb-40 md:gap-x-16 lg:gap-x-28">
            <div class="flex flex-col items-center justify-center text-white mb-8 md:mb-16">
                <h1 class="block-effect" style="--td: 1.2s">
                    <div class="block-reveal text-3xl lg:text-5xl " style="--bc: #15803d; --d: .1s">Welcome to</div>
                    <div class="block-reveal text-5xl lg:text-7xl text-primary font-medium" style="--bc: #041A29; --d: .5s">My JS games</div>
                </h1>
            </div>
            <div class="flex items-end justify-center mt-16 mb-20 md:m-10">
                <GameSlider class="overflow-hidden"/>
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


<style scoped>
p {
  color: #2e2e2e;
  margin-bottom: 20px;
}


/* block-$ */
.block-effect {
  font-size: calc(8px + 6vw);
}

.block-reveal {
  --t: calc(var(--td) + var(--d));

  color: transparent;
  padding: 4px;

  position: relative;
  overflow: hidden;

  animation: revealBlock 0s var(--t) forwards;
}

.block-reveal::after {
  content: '';

  width: 0%;
  height: 100%;
  padding-bottom: 4px;

  position: absolute;
  top: 0;
  left: 0;

  background: var(--bc);
  animation: revealingIn var(--td) var(--d) forwards, revealingOut var(--td) var(--t) forwards;
}


/* animations */
@keyframes revealBlock {
  100% {
    color: #0f0f0f;
  }
}

@keyframes revealingIn {

  0% {
    width: 0;
  }

  100% {
    width: 100%;
  }
}

@keyframes revealingOut {

  0% {
    transform: translateX(0);
  }

  100% {
    transform: translateX(100%);
  }

}

</style>
