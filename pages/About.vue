<template>
  <div class="container">
    <h1> About DadJokes</h1>
    <p>This is an app that displays shitty dad jokes</p>
  </div>
</template>

<script>
export default{
  head(){
    return{
      title:"About This",
      meta:[
        {
          hid:"description",
          name:"description",
          content: "Great dad jokes"
        }
      ]
    }
  }
}
</script>

<style scoped>
h1,
p{
  text-align: center;
}
</style>