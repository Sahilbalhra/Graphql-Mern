/**All Query**/

//client queries
{
    client(id:1){
        name
        email
        id
    }
},
{
  clients{
    id,
    name,
    email,
    phone
  }
},

//Project queries
{
  project(id:1){
    id,---------------
    name,            - 
    status,          -
    description,     -Both id will be same 
    client{          -
      id--------------
      name
      email
    }
  }
},
{
  projects{
    id,
    name,
    status,
    description,
  }
}

/**Mutation**/
mutation{
  addClient(name:"amit",email:"amit@gmail.com",phone:"1231-213-2131"){
    id
    name
    email
    phone
  }
},
mutation{
  deleteClient(id:"63184f743ca7943b6a748a4e"){
    id
    name
    email
    phone
  }
},
mutation{
  updateClient(id:"63184f243ca7943b6a748a4c",name:"rahul",email:"rahul@gmail.com"){
    id
    name
    email
  }
},

mutation{
  addProject(name:"jdkas",description:"A good initiative for school and colleges23",clientId:"6318515a5b1ce37cc6142439"){
    id
    name
    description
    
  }
}

mutation{
  deleteProject(id:"631856a68b4420fdba4c6d9b"){
    id
    name
    status
    description
    client{
     name
      email
   } 
  }
}
mutation{
  updateProject(id:"631855b8e77523971c591c89",name:"js",description:"jbskjcascbasb",status:"Completed"){
    id
    name
    description
  }
}