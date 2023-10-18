<template>
    <div>
        <input 
            type="text" 
            placeholder="Title"
            v-model="post.title"
        /> 
        <input 
            type="text" 
            placeholder="Body" 
            v-model="post.body"
        />
        <button
            @click="createPost"
        >Create</button>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                post: {
                    title:"",
                    body:""
                }
            }
        },
        methods: {
            createPost(){
                this.post.id = Date.now();
                this.$emit('create', this.post);
                this.post = {
                    title:"",
                    body:"" 
                }
            }
        }
    }
</script>

<style>

</style>