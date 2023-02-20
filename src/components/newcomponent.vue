<template>
<div class="newdiv">
    <h1> New component </h1>
   <users data="user 1"/>
    <users data="user 2"/>

</div>

</template>
<script>
import users from "./users.vue"

export default {
    name:"Home_app",
    components:{
        users

    },
    props:{
        data:String,
        
    },
    data()
    {
        return{
            show:true,
        
        }
    },

    methods:{
        hello(){
          
            
        }
    }

  
}
</script>

<style scoped>
.newdiv{
    background-color: cadetblue;
    height: 100%;
}

</style>
