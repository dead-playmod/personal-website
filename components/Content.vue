<template>
    <main>
        <slot />
    </main>
</template>

<script>
export default {
    name: 'Content'
}
</script>

<style scoped>
main {
    height: 100%;
    width: 100%;
    overflow-y: scroll;
}

::-webkit-scrollbar {
    width: 10px;
}
::-webkit-scrollbar-thumb {
    background: rgba(255, 255, 255, 0.25);
}
::-webkit-scrollbar-thumb:hover {
	background: rgba(255, 255, 255, 0.5);
}
</style>