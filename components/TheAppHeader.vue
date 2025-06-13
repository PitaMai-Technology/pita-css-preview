<template>
    <header>
        <div class="logo-container hide-max768">
            <NuxtLink to="/">
                PitaCSS(α)
            </NuxtLink>
        </div>
        <div class="logo-container-responsive hide-min768">
            <NuxtLink to="/">
                PitaCSS(α)
            </NuxtLink>
        </div>
    </header>
</template>

<script setup>
</script>

<style>

.logoText {
    font-size: var(--smallMediumFontSize, 1.5rem);
    font-weight: 700;
    color: var(--mainColor, #b8fb97);
    margin: 0;
    padding: 0;
}

.headerRight {
    display: flex;
    align-items: center;
    gap: 1.5rem;
}
</style>