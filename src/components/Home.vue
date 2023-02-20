<template>
<div>
    <h1> Hello from home component {{data}}</h1>
    <h1 v-if="show">If block</h1>
     <h1 v-else>Else block</h1>
    <button v-on:click ="hello" >click here</button>
    <table>
        <tr>
            <td>ID</td>
            <td>Name</td>
            <td>Email</td>
        </tr>
          <tr v-for="user in users" :key="user.id">
            <td>{{user.id}}</td>
            <td>{{user.name}}</td>
            <td>{{user.email}}</td>
        </tr>
    </table>

</div>

</template>
<script>


export default {
    name:"Home_app",
    props:{
        data:String,
        
    },
    data()
    {
        return{
            show:true,users:[
                {id:1,name:"ham",email:"ham@gmail.com"},
                {id:2,name:"jam",email:"jam@gmail.com"},
                {id:3,name:"ram",email:"ram@gmail.com"},
                {id:4,name:"sam",email:"sam@gmail.com"}
            ]
        
        }
    },

    methods:{
        hello(){
            this.show=!this.show
            
        }
    }

  
}
</script>
