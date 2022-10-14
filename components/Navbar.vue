<template>
    <nav>
        <ul>
            <li>
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/characters">Characters</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/characters/3">Character 3</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/404">triggerr Error</NuxtLink>
            </li>
        </ul>
        <button @click="triggerError">Trigger an Error</button>
    </nav>
</template>
<script setup lang="ts">
const triggerError = () => {
    showError("😱 Oh no, an error has been thrown.")

}
</script>

<style>
.router-link-active {
    background-color: aqua;
}
</style>
