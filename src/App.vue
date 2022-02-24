<template>
  <div class="flex flex-col pt-10 mb-5">
    <h1 class="text-4xl font-bold text-center">Cat Clicker 🐱</h1>
    <div class="flex flex-col md:flex-row  justify-around">
      <div v-for="cat in cats" :key="cat.name">
        <counter
          class="p-10"
          :cat="cat"
          v-model="cat.counter"
          @event-increment="cat.counter++"
        />
      </div>
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
      cats: [
        { catName: "Doraemon", image: "doraemon.png", counter: 0},
        { catName: "Garfield", image: "garfield.png", counter: 0},
      ],
    };
  },
};
</script>

<style scoped>
/*
body {
  padding: 10vh;
  margin-top: 60px;
}
.container {
  display: flex;
  flex-direction: column;
}
.text-center {
  text-align: center;
}

.cat-container {
  display: flex;
  flex-wrap: wrap;
  margin: 0 auto;
}

.cat-display {
  max-width: 45%; 
  margin: 0 auto;
  margin-bottom: 2em;
}

*/
</style>
