<template>
    3秒後にローディング(SSR)が完了します。
</template>

<script setup>
await new Promise(resolve => setTimeout(resolve, 3000))
</script>