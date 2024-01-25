<template>
  <div class="relative h-full -mt-20">
    <div class="relative flex items-center justify-center h-[100vh]">
      <div class="flex items-center justify-center max-w-full">
        <div class="flex flex-col items-start text-white m-8">
          <h1 class="text-xl sm:text-3xl md:text-5xl mb-1 sm:mb-2 md:mb-4">
            Welcome to
          </h1>
          <h1 class="text-3xl sm:text-5xl md:text-7xl text-primary font-medium">
            My JS games
          </h1>
        </div>
      </div>

      <div class="custom-shape-divider-bottom absolute bottom-0 z-30">
        <svg
          data-name="Layer 1"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 1200 120"
          preserveAspectRatio="none"
        >
          <path
            d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
            opacity=".25"
            class="shape-fill-black"
          ></path>
          <path
            d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
            opacity=".5"
            class="shape-fill-black"
          ></path>
          <path
            d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
            class="shape-fill-black"
          ></path>
        </svg>
      </div>
    </div>
    <GameGalery :games="juegos" />
    <div class="custom-shape-divider-bottom absolute bottom-0 z-30">
      <svg
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
      >
        <path
          d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
          opacity=".25"
          class="shape-fill-green"
        ></path>
        <path
          d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
          opacity=".5"
          class="shape-fill-green"
        ></path>
        <path
          d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
          class="shape-fill-green"
        ></path>
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
  fill: #060b23;
}

.custom-shape-divider-bottom .shape-fill-green {
  fill: #22c55e;
}
</style>

<script setup>
const juegos = [
  {
    id: 1,
    name: "Flappybird",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
    image: "/flappy-bird.png",
    href: "/games/flappyBird",
    ringcolor: "hover:ring-primary",
    iconcolor: "text-primary",
    isRight: false,
  },
  {
    id: 2,
    name: "Blackjack",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
    image: "/blackjack.jpg",
    href: "/games/blackjack",
    ringcolor: "hover:ring-lime-600",
    iconcolor: "text-lime-600",
    isRight: true,
  },
  {
    id: 3,
    name: "Naval Battle",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
    image: "/naval-battle.png",
    href: "/games/naval-battle",
    ringcolor: "hover:ring-sky-400",
    iconcolor: "text-sky-400",
    isRight: false,
  },
  {
    id: 4,
    name: "Pac-man",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
    image: "pac-man.avif",
    href: "/games/pac-man",
    ringcolor: "hover:ring-yellow-400",
    iconcolor: "text-yellow-400",
    isRight: true,
  },
  {
    id: 5,
    name: "Tetris",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
    image: "/tetris.webp",
    href: "/games/tetris",
    ringcolor: "hover:ring-blue-500",
    iconcolor: "text-blue-500",
    isRight: false,
  },
  {
    id: 6,
    name: "Juego Clase",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dictum iaculis dui, non volutpat ante rhoncus vel. Fusce cursus dui non vestibulum facilisis. Curabitur pretium id nunc et molestie. Phasellus aliquam neque ac ipsum facilisis, vel rutrum libero lacinia. Sed porttitor tempus nisi id eleifend. Etiam ornare augue quis consequat facilisis.",
    image: "",
    href: "/games/juego-clase",
    ringcolor: "hover:ring-indigo-600",
    iconcolor: "text-indigo-600",
    isRight: true,
  },
];
</script>
