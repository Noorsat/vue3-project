<template>
  <post-form 
    @create="createPost"
  />
  <post-list 
    :posts="posts" 
    @remove="removePost"
  />
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {
    PostForm,
    PostList
  },
  data() {
    return {
      posts: [],
    }
  },
  methods: {
    createPost(post){
      this.posts.push(post);
    },
    removePost(id){
      this.posts = this.posts.filter(post => post.id !== id)
    }
  }
}
</script>

<style>
</style>