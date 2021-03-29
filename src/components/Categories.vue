<template>
<div class="container">
    <div :key ="index"  v-for="(category,index) in categories">
        <h1>{{category.name}}
            <Button  @click = "collectMeetingInput(index)" text = "+"></Button>
            <i @click = "$emit('delete-category', category)"  class="fas fa-window-close"></i>
        </h1>       
        <Meeting @delete-meeting = "$emit('delete-meeting',{meeting:$event,index})" :category="category"/>
    </div>
</div>
    
</template>

<script>
import Meeting from "./Meeting"

export default {
    name: "Categories",
    props: {
        categories: Array
    },
    components:{
        Meeting,
    },
    methods: {
        collectMeetingInput(index){
            let x = {}; 
            x.zoomName = prompt("Enter zoom meetings"); 
            x.zoomLink = prompt("Enter zoom link"); 
            x.zoomPass = prompt("Enter zoom pass"); 
            this.$emit('add-meeting', {x,index})
        }
    },
    emits: ["delete-meeting","delete-category","add-meeting"],
}
</script>
