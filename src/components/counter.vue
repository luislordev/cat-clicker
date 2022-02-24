<template>
  <div class="flex flex-col md:flex-row items-center">
    <div class="text-center">
      <h2 class="p-3 font-bold text-2xl uppercase">{{ cat.name }}</h2>
      <cat :image="cat.image" @click="increment()" />
    </div>

    <div class="text-center">
      <h2 class="text-lg font-bold tracking-wide text-gray-700">Veces pulsado:</h2>
      <h3 class="font-extrabold">{{ cat.counter }}</h3>
    </div>
  </div>
</template>

<script>
import cat from "./cat.vue";
export default {
  components: { cat },
  name: "Counter",
  props: {
    cat: {
      type: Object,
      require: true,
    },
  },
  methods: {
    increment() {
      this.$emit("event-increment");
    },
  },
};
</script>

<style scoped>
</style>