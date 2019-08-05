<template>
  <div class="joke">
    <p>{{ joke }} </p>
  </div>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"]
}
</script>

<style>
<style>