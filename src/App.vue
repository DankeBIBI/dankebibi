<template>
    <router-view v-slot="{ Component }">
        <transition>
            <component :is="Component"></component>
        </transition>
    </router-view>
</template>

<style lang="scss">
</style>
