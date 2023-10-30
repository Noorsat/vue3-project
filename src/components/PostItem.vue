<template>
    <div class="post" style="display: flex; align-items: center; gap:30px;">
        <div>
            <div>
            <strong>Название:</strong> {{ post.title }}
            </div>
            <div>
                <strong>Описание:</strong> {{ post.body }}
            </div>
        </div>
        <div>
            <my-button
                @click="$emit('remove', post.id)"
            >
                Delete
            </my-button>
        </div>
    </div>
</template>

<script>

    export default {
        props: {
            post: {
                type: Object,
                required: true
            }
        },
    }
</script>

<style>

</style>