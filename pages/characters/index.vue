<template>
    <div>
        List of characters:
        <ol>
            <li 
                v-for="character in characters.results"
            >
                <NuxtLink :to="`/characters/${character.id}`">
                    {{character.id}} - {{character.name}}
                </NuxtLink>
            </li>
        </ol>
    </div>

</template>

<script setup lang="ts">
const { data: characters } = await useFetch('https://rickandmortyapi.com/api/character', { pick: ['results'] })
</script>   