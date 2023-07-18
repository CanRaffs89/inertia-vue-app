<template>
    <div class="container">
        <h1>User List</h1>
        <Link class="button" href="/users/create">Add New User</Link>
        <slot />
    </div>
</template>

<script setup>
    import { Link } from '@inertiajs/vue3';
</script>

<style lang="scss" scoped>

</style>