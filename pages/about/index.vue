<template>
    <div class="w-full h-full overflow-hidden flex">
        <div class="w-3/4 mx-auto flex flex-col justify-center card">
            <div
            class="mx-auto icon-background">
                <div class="text-9xl rounded-full icon">
                    :3
                </div>
            </div>
            <div class="border border-white border-solid p-9 rounded-xl">
                <h1 class="text-4xl text-center font-semibold mb-8">Hey, my name is Marcin.</h1>
                <p class="text-lg">
                    I'm a beginner front-end developer mostly accustomed to <a href="https://vuejs.org/" target="_blank" class="text-green-500 underline">VueJS</a> and <a href="https://nuxtjs.org/" target="_blank" class="text-green-300 underline">NuxtJS</a>, with some experience in <a href="https://unity.com/" target="_blank" class=" text-gray-500 underline">Unity Game Engine</a> and <a href="https://docs.microsoft.com/pl-pl/dotnet/csharp/tour-of-csharp/" target="_blank" class=" text-purple-400 underline">C#</a>
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.card {
    transform: translateY(-5rem);
}
@keyframes spin {
	from {
		transform: rotateY(0deg);
	}
	to {
	    transform: rotateY(360deg);
	}
}
.icon {
    width: 10rem;
    height: 10rem;
    flex-shrink: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    animation-name: spin;
	animation-duration: 3s;
    animation-delay: 250ms;
    animation-iteration-count: infinite;
    animation-timing-function: ease-out;
}
.icon-background {
    border: white solid 1px;
    background: radial-gradient(circle, rgba(0,0,0,1) 0%, rgba(42,0,72,1) 75%);
    border-radius: 100%;
    position: relative;
    top: 2rem;
    width: 10rem;
    height: 10rem;
    flex-shrink: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>