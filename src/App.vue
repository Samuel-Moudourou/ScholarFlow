<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>

<RouterView v-slot="{Component}">
    <Transition name="page" mode="out-in">
        <Component :is="Component" />
    </Transition>
</RouterView>
</template>

<style>
.page-enter-active,
.page-leave-active {
    transition: 600ms ease all;
}

.page-enter-from,
.page-leave-to{
    opacity: 0;
}
</style>

