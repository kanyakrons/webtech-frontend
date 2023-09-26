<template>
    <nav class="flex text-black">
        <MenuLink to="/">Home</MenuLink>
        <MenuLink to="/artist">Artist</MenuLink>
        <MenuLink to="/artist/create">Add Artist</MenuLink>
        <MenuLink to="/logout">Logout</MenuLink>
        <div class="inline-block px-4 py-2 bg-black text-white">
            {{ auth.user.name }}
        </div>
    </nav>
</template>

<script setup lang="ts">
  import { useAuthStore } from '~/stores/useAuthStore'
  const auth = useAuthStore()
  </script>