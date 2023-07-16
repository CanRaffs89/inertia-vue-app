<template>
    <Link :href="'/users/' + user.id">
        <div class="user-card">
            <h2>{{ user.name }}</h2>
            <h3>{{ user.email }}</h3>
        </div>
    </Link>
</template>

<script setup>
    import { Link } from '@inertiajs/vue3';

    const props = defineProps([
        'user'
    ]);
</script>

<style lang="scss" scoped>

</style>