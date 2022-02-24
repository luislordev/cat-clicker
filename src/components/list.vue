<template>
  <div class="">
    <h2 class="text-3xl font-bold">Gatitos famosos</h2>
    <div>
      <ul>
        <li
          v-for="item in listItems"
          :key="item.id"
          @click="selected(item.id)"
          class="text-lg my-5 pl-5 p-2 cursor-pointer border-2 rounded-2xl"
          :class="[item.id == activeItem ? 'font-bold' : '']"
        >
          {{ item.name }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "List",
  data() {
    return {
      activeItem: 0,
    };
  },
  props: {
    listItems: {
      type: Array,
      require: true,
    },
  },
  methods: {
    selected(id) {
      this.activeItem = id;
      this.$emit("item-selected", id);
    },
  },
};
</script>

<style>
</style>