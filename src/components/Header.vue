<template>
   <header>
        <h1>{{title}}</h1>
    </header>
</template>
   

<script>

export default {
    name: "Header", 
    props: {
        title: String, 
    },
    components:{
    },
    methods: {
        collectCategoryInput(){
            console.log("test")
            let x = {}; 
            x.name = prompt("Enter category name"); 
            x.meetings = []; 
            this.$emit('add-category', x)
        },
        toggleNavbar: function(){
      this.showMenu = !this.showMenu;
    }
    },
    emits:["add-category"],
}
</script>

<style scoped>
    header{
        display: flex; 
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>
