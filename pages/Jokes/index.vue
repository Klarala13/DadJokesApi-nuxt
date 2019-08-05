<template>
  <div>
    <Joke v-for="joke in jokes" v-bind:key="joke.id" :id="joke.id" :joke="joke.joke"/>
  </div>
</template>

<script>
import axios from "axios";
import Joke from "../../components/Joke";

export default {
  components:{
    Joke
  },
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
      title: this.joke,
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