<template>


</template>



<script>
export default {
    name: "Meeting",
    props:{
        category: Object 
    },
    methods: {
        alert(id){
          console.log(id)
        }
    },
    emits: ["delete-meeting"]
}
</script>

<style scoped>
a{
    text-decoration: none;
}
a:visited{
    text-decoration: none;
}
.fas {
  color: rgb(255, 255, 255);
}
.task {
  background: #d1d1d1;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid rgb(0, 0, 0);
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

</style>