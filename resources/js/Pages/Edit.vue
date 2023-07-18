<template>
    <Layout>
        <h1>Edit User {{ user.name }}</h1>
        <form @submit.prevent="updateUser">
            <div class="container">
                <input type="text" placeholder="Enter name..." v-model="updateForm.name">
                <input type="email" placeholder="Enter email" v-model="updateForm.email">
                <input type="password" placeholder="Enter password" v-model="updateForm.password">
                <button>Update User</button>
            </div>
        </form>
    </Layout>
</template>

<script setup>
    import { useForm } from '@inertiajs/vue3';
    import Layout from '../Layout.vue';

    const props = defineProps([
        'user'
    ]);

    // Prefill the form with the user's previous values
    const updateForm = useForm({
        name: props.user.name,
        email: props.user.email,
        password: '',
    });

    // Send a patch request to users/userID to update values
    const updateUser = () => {
        updateForm.patch("/users/" + props.user.id);
    };
</script>

<style lang="scss" scoped>

</style>