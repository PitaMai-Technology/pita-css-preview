<script setup>

let progressLoader = null

onMounted(async () => {
await import('pita-css/js')
});

onUnmounted(() => {
  progressLoader?.destroy()
})

</script>

<template>
    <div>
        <NuxtLayout>
            <NuxtRouteAnnouncer />
            <NuxtPage />
        </NuxtLayout>
    </div>
</template>

<style>
#progress {
    height: 4px;
    z-index: 1000;
    width: 100%;
}

.fade-enter-active {
    transition: opacity 0.2s ease-in;
}

.fade-leave-active {
    transition: opacity 0.5s ease-out;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>