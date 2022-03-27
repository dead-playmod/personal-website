<template>
    <div class="min-h-screen overflow-hidden">
        <Header />
        <Nuxt class="page-content" />
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Content from '@/components/Content.vue'

export default {
    components: {
        Header,
        Content
    }
}
</script>

<style scoped>
.page-content {
    height: calc(100vh - 5rem);
}
.page-scroll {
    overflow-y: scroll;
}

@keyframes header-slide {
	0% {
		opacity: 0;
		transform: translateY(-100%);
	}
	60% {
		opacity: 0;
		transform: translateY(-100%);
	}
	100% {
		opacity: 1;
		transform: translateY(0);
	}
}
.header-slide {
	animation-name: header-slide;
	animation-duration: 2.75s;
	animation-timing-function: ease-out;
}
</style>