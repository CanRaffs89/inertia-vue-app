<template>
    <Layout>
        <div class="user-card">
            <h1>{{ user.name }}</h1>
            <h3>{{ user.email }}</h3>
            <Link :href="'/users/' + user.id + '/edit'">Edit User</Link>
            <Link method="delete" :href="'/users/' + user.id">Delete User</Link>
        </div>
    </Layout>
</template>

<script setup>
    import { Link } from '@inertiajs/vue3';
    import Layout from '../Layout.vue';
    const props = defineProps([
        'user'
    ]);
</script>

<style lang="scss" scoped>

</style>