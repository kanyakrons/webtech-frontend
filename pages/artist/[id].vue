<template>
    <h1>{{ pageTitle }}</h1>

    <div class="text-3xl mx-4">
        {{ artist.name }}
    </div>

    <div v-for="song in artist.songs" :key="song.id">
        <div class="text-xl mx-6 my-2">
            {{ song.title }}
        </div>
    </div>
</template>

<script setup lang="ts">
const route = useRoute()
const pageTitle = `Artist No. ${route.params.id}`
const { data:artist } = await useMyFetch<any>(
    `artist/${route.params.id}`, {}
)
</script>