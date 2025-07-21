<template>
    <div
        class="image-button text-indigo-300 dark:text-indigo-700 hover:text-indigo-500 active:text-indigo-700 dark:active:text-indigo-300 cursor-pointer transition-colors">
        <slot />
    </div>
</template>

<style scoped>
.image-button:active {
    animation: expressive-bounce 0.5s ease-in-out;
}
</style>
