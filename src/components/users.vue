<template>
<div class="userdiv">
    <h1> {{data}} </h1>
       <button v-bind:disabled="show" >click here</button>
   

</div>

</template>
<script>


export default {
    name:"Users_App ",
    props:{
        data:String,
        
    },
    data()
    {
        return{
            show:false,
        
        }
    },

    methods:{
        hello(){
          
            
        }
    }

  
}
</script>

<style scoped>
.userdiv{
    background-color:blueviolet;
    height: 300px;
    width: 50%;
    position: relative;
    top: 10%;
    left:10%;
}

</style>
