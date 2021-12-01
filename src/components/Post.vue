<template>
    <div>
    
        
    <PostItem
    
            v-for="post in posts"
            v-bind:key="post.title" :post="post"
            @post-item-changed="Changed"/>
    </div>
        
    



  
</template>

<script>
import PostItem from './components/PostItem.vue'
export default {
    props: ['posts'],
    componenets: {PostItem},
    methods: {
        Changed(e) {
            this.$emit('post-title-changed', e),
            this.$emit('post-body-changed', e)
        }


    }
}
</script>

<style>

</style>