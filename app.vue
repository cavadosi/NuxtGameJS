<template>
	<body >
		<NuxtLayout>
			<NuxtPage />
		</NuxtLayout>
	</body>
</template>


<style>

html {
	background: url('/background.png') no-repeat center center fixed;
	background-size: cover;
	height: 100%;
}

body {
	background-color: radial-gradient(circle, rgba(6,11,35,1) 100%, rgba(2,4,32,1) 100%);
	min-height: 100%;
	margin: 0;
	position: relative;
	z-index: 1;
}

body::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	opacity: 0.5;
	z-index: -1;
	background-size: cover;
}
</style>