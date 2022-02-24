<template>
  <div class="flex flex-col pt-10 mb-5">
    <h1 class="text-4xl font-bold text-center">Cat Clicker 🐱</h1>
    <div class="flex flex-col md:flex-row  justify-around pt-10 ">
      <list class="mx-auto" :listItems="cats" @item-selected="($event) => selectedCat = $event"/>
        <counter
          class="mx-auto"
          :cat="item"
          v-model="item.counter"
          @event-increment="item.counter++"
        /> 
    </div>
  </div>
</template>

<script>
import Counter from "./components/counter.vue";
import List from './components/list.vue';
export default {
  components: { Counter, List },
  name: "App",
  data() {
    return {
      selectedCat: 0,
      cats: [
        {id: 0, name: "Doraemon", image: "doraemon.png", counter: 0},
        {id: 1, name: "Garfield", image: "garfield.png", counter: 0},
        {id: 2, name: "Hello Kitty", image: "helloKitty.png", counter: 0},
        {id: 3, name: "Tom", image: "tom.png", counter: 0},
        {id: 4, name: "Gato con botas", image: "gatoConBotas.png", counter: 0},
      ],
    };
  },
  computed: {
    item() {
      return this.cats[this.selectedCat];
    }
  },
};
</script>

<style scoped>

</style>
