<template>
<div class="datadiv">
    <h1> ToDo List </h1>

    <input class="intxt" type="text" name="add" id="Add" v-model="message" >

       <button class="btn" v-on:click="addToDo(message)">ADD</button> <br />
 
   

<div class="container">
    <div class="heading">
       
         <div class="col">Task</div>
        
         <div class="col">Delete </div>
          <div class="col">Status</div>
    </div>
    <div class="table-row" v-for="user in todo" :key="user.id" >  
        
        
         <div class="col" v-if="user.status"><del>{{user.name}}</del></div>
          <div class="col" v-else>{{user.name}}</div>
       
        
         <div class="col"><img class="delimg" src="../assets/delete.png" v-on:click="delToDo(user.id)"/></div>
         <div class="col" v-if="user.status"><img class="delimg" src="../assets/accept.png"  v-on:click="updateToDo(user.id)"/></div>
         <div class="col" v-else><img class="delimg" src="../assets/warndone.png" v-on:click="updateToDo(user.id)"/></div>
 <p v-show=false>  {{ idd=user.id}}</p>
    </div>
 

    
    </div>

   
            
           
</div>

        
           
 
          
        


</template>
<script>


export default {
    name:"DataBind ",
    props:{
        data:String,
        
    },
    data()
    {
        return{
            show:false,
            idd:0,
            message:"",
            todo:[
                {id:1,name:"Need to complete vue prooject",status:false},
             
               
            ],
        
        }
    },

    methods:{
        addToDo(data){
           // console.log(data);
          
            this.todo.push({id:this.idd+1,name:data,status:false});
            
        },
          delToDo(data){
           // console.log(data);
          data=data-1;
            this.todo.splice(data,1);
           this. idd--;
            
        },
           updateToDo(data){
            //console.log(data);
            this.todo[data-1].status=!this.todo[data-1].status;
    
            
        },
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



.container{
    display:table;
    width:90%;
    border-collapse: collapse;
    }
 .heading{
     font-weight: bold;
     display:table-row;
     background-color:aquamarine;
     text-align: center;
     line-height: 25px;
     font-size: 20px;
     font-family:georgia;
     color:black;
     border: 2px solid black;
 }
 .table-row{  
     display:table-row;
     text-align: center;
 }
 .col{ 
    display:table-cell;
     border: 1px solid black;
     font-size: 20px;
     font-family:georgia;
 }
.intxt{
     background-color:rgb(131, 205, 236);
    height:50px;
    width: 50%;
  

}
.btn{
     height:50px;
    width:80px;
 
     background-color:rgb(60, 98, 186);
}

.delimg{
    padding: 10px;
 height:35px;
    width: 30%;
}
</style>



