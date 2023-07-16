<template>
    <div class="container">
        <h1>Todo List</h1>
        <div>
            <User 
                v-for="user in users"
                :key="user.id"
                :user="user"
            />
        </div>
    </div>
</template>

<script setup>
    import User from '../Components/User.vue';

    const props = defineProps([
        'users'
    ]); 
</script>

<style lang="scss" scoped>

</style>