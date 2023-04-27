<template>
  <section>
    <center>
    <h1>{{ name }}</h1>
    <button @click="showDetails()">Show Details</button>
    <ul v-if="detailsAreVisabled">
      <li>{{ id }}</li>
      <li>{{ name }}</li>
      <li>{{ emailAddress }}</li>
      <li>{{ phoneNumber }}</li>
    </ul>
    </center>
  </section>
</template>
<script>
export default {
 props:[
'id',
'name',
'emailAddress',
'phoneNumber'
 ],
  data() {
    return {
    
      detailsAreVisabled: false,
      friends: 
        {
          id: "manuel",
          name: "Manuel Lorenz",
          phone: "0390320302",
          email: "manuel@gmail.com",
        },
        
    
    }
},
      methods: {
        showDetails() {
          this.detailsAreVisabled = !this.detailsAreVisabled;
          console.log(this.friends);
        },
      }
  
}
</script>