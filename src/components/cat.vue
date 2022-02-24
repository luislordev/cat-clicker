<template>
  <div>
    <img
    class="h-80 w-80 cursor-pointer"
      :src="require(`@/assets/images/${image}`)"
      :alt="image"
      :title="image"
    />
  </div>
</template>

<script>
export default {
  name: "Cat",
  props: {
    image: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
</style>