<template>
    1秒後にローディング(SSR)が完了します。
</template>

<script setup>
await new Promise(resolve => setTimeout(resolve, 1000))
</script>