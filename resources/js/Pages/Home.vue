<template>
    <Layout>
        <Link :href="'/users/create'">Add New User</Link>
        <div>
            <User 
                v-for="user in users"
                :key="user.id"
                :user="user"
            />
        </div>
    </Layout>
</template>

<script setup>
    import { Link } from '@inertiajs/vue3';
    import Layout from '../Layout.vue';
    import User from '../Components/User.vue';
    import CreateUserForm from '../Components/CreateUserForm.vue';

    const props = defineProps([
        'users'
    ]); 
</script>

<style lang="scss" scoped>

</style>