<template>
  <div>jokes</div>
</template>

<script>
import axios from "axios";

export default {
  data(){
    return{
      jokes: []
    }
  },

 async created(){
    const config ={
      headers: {
        "Accept": "application/json"
      }
    }
    try { 
    const res = await axios.get("https://icanhazdadjoke.com/search", config);
      //console.log(res.data);
      this.jokes = res.data.results;
    }catch (err) {
      console.error(err)
    }
  },
  head(){
    return{
      title:"DadJokes",
      meta:[
        {
          hid:"description",
          name:"description",
          content: "Great dad jokes"
        }
      ]
    }
  }
};
</script>