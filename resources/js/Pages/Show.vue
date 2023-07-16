<template>
    <div class="user-card">
        <h1>{{ user.name }}</h1>
        <h3>{{ user.email }}</h3>
    </div>
</template>

<script setup>
    const props = defineProps([
        'user'
    ]);
</script>

<style lang="scss" scoped>

</style>