<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="text"
      placeholder="Search for Jokes...">
    <input type="submit" class="btn-dark" value="Search Jokes">
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return{
      text:""
    };
  },
  methods:{
    onSubmit(){
      this.$emit("search-text", this.text);
      this.text = "";
    }
  }
};
</script>

<style scoped>
  input{
    padding: 1rem;
    margin: 1rem;
  }
<style>