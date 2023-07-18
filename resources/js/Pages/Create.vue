<template>
    <Layout>
        <form @submit.prevent="createUser">
            <div class="container">
                <input type="text" placeholder="Enter name..." v-model="userForm.name">
                <input type="email" placeholder="Enter email" v-model="userForm.email">
                <input type="password" placeholder="Enter password" v-model="userForm.password">
                <button>Add User</button>
            </div>
        </form>
    </Layout>
</template>

<script setup>
    import { useForm } from '@inertiajs/vue3';
    import Layout from '../Layout.vue';

    const userForm = useForm({
        name: '',
        email: '',
        password: ''
    });

    const createUser = () => {
        userForm.post('/users');
    };
</script>

<style lang="scss" scoped>

</style>