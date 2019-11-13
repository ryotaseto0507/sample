<template>
    <div>
        <h2>Title</h2>
        <input type="text" v-model="title" >
        <h2>Content</h2>
        <textarea v-model="content"></textarea>
        <button  @click="addNewpage(title,content)" >
            Create
        </button>
    </div>
</template>
<script>
export default {
    head: {
        title: 'New Page'
    },
    data: function(){
        return{
            title: '',
            content:'',
        }
    },
    methods: {
       addNewpage(text1,text2){
           this.$store.dispatch('addNewpage',{id: this.$store.getters.max,title:text1,content:text2})
       } 
    }

}
</script>
<style scoped>
input,textarea{
    color: black;
    background-color: white;
}
</style>