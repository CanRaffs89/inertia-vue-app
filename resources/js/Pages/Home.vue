<template>
    <Layout>
        
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
    import Layout from '../Layout.vue';
    import User from '../Components/User.vue';

    const props = defineProps([
        'users'
    ]); 
</script>

<style lang="scss" scoped>

</style>