<template>
	<div>
		<main class="flex justify-center items-center overflow-hidden h-full w-full gradient">
			<p class="z-10 text-5xl text-center text">
				Hey! 
				<br>
				Welcome to my website.
			</p>
		</main>
	</div>
</template>

<script>
export default {
}
</script>

<style scoped>
@keyframes gradient-fade {
	from {
		background-position-y: -100%;
		opacity: 0;
	}
	to {
		background-position-y: 0;
		opacity: 1;
	}
}
.gradient {
	background: linear-gradient(0deg, rgba(154,0,255,0.75) 0%, rgba(0,0,0,1) 75%);
	opacity: 1;
	animation-name: gradient-fade;
	animation-duration: 1.75s;
	animation-timing-function: ease;
}
@keyframes text-fade {
	0% {
		opacity: 0;
		transform: translateY(-40px);
	}
	60% {
		opacity: 0;
		transform: translateY(-40px);
	}
	100% {
		opacity: 1;
		transform: translateY(-80px);
	}
}
.text {
	transform: translateY(-80px);
	animation-name: text-fade;
	animation-duration: 2s;
	animation-timing-function: ease;
}
</style>
