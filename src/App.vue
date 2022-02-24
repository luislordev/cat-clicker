<template>
  <div class="container">
    <h1 class="text-center">Cat Clicker 🐱</h1>
    <div>
      <counter
        :cat="cat"
        v-model="cat.counter"
        @event-increment="cat.counter++"
      />
    </div>
  </div>
</template>

<script>
import Counter from "./components/counter.vue";
export default {
  components: { Counter },
  name: "App",
  data() {
    return {
       cat: {
        catName: 'doraemon', 
        image:'doraemon.png',
        counter: 0
      }
    };
  },
};
</script>

<style scoped>
* {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
body {
  padding: 1vh;
  margin-top: 60px;
}
.container {
  display: flex;
  flex-direction: column;
}
.text-center {
   text-align: center;
}
</style>
