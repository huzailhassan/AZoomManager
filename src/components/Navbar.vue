<template>
<div>
  <v-toolbar
    color="#242424"
    class="font-weight-bold">
    <v-toolbar-title>Zoom Manager</v-toolbar-title>
  </v-toolbar>
</div>
</template>

<script>
export default{
    name: "Navbar",
    components:{
    },
    data(){
        return{
            drawer: null,
            dialog: false
        }
    },
}
</script>
