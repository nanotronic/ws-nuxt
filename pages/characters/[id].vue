
<template>
    <div>
        <div>character with id: {{ character.id }}</div>
        <div>Name: {{character.name}}</div>
        <div>Location: {{character.location.name}}</div>
        <img class="avatar" :src="character.image">
    </div>
</template>


<script setup lang="ts">
const route = useRoute()
const id = route.params.id
const { data: character } = await useFetch(`https://rickandmortyapi.com/api/character/${id}`, { pick: ['id', 'name', 'location', 'image'], key: id })

// watch(id, async (count, prevCount) => {
//     const { data } = await useFetch(`https://rickandmortyapi.com/api/character/${id}`, { pick: ['id', 'name', 'location', 'image'], key })
//     character =  data
// })
</script>

<style>
.avatar {
    width: 100px;
    height: 100px;
}
</style>
