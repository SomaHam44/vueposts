<template>
    <div>
    
        
        <PostItem
         />
        <ul>
            <li 
            v-for="post in posts"
            v-bind:key="post.title" :title="post.title"
            @post-item-changed="Changed"
            > {{post.title}}
            <button>Edit</button></li>
            </ul>
    

    </div>
        
    



  
</template>

<script>
import PostItem from './components/PostItem.vue'
export default {
    props: ['posts'],
    componenets: {PostItem},
    methods: {
        Changed(e) {
            this.$emit('post-item-changed', e)
        }


    }
}
</script>

<style>

</style>