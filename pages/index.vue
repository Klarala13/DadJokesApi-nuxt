<template>
  <div class="container">
   <h2>Welcome to DadJokes</h2>
   <p> This is a simple SPA where you can search for jokes and display them. It uses Vue, routing and Nuxt to accomplish it´s very few utilities. </p>
  </div>
</template>

<script>
export default {
 head(){
    return{
      meta:[
        {
          hid:"description",
          name:"description",
          content: "Great dad jokes",
        }
      ]
    }
  }
}
</script>

