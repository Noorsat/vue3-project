<template>
    <post-item 
        v-for="post in posts"
        :post="post"
        :key="post.id"
        @remove="$emit('remove', post.id)"
    />
</template>


<script>
    import PostItem from '@/components/PostItem.vue';

    export default {
        components: {
            PostItem
        },
        props: {
            posts: {
                type: Array,
                required: true
            }
        }
    }
</script>

<style>

</style>