<template>
  <div>
      <img :src="require(`@/assets/images/${image}`)" :alt="image" :title="image"/>
  </div>
</template>

<script>
export default {
    name: 'Cat',
    props: {
        image: {
            type: String,
            required: true
        }
    }

}
</script>

<style scoped>
img {
    width: 300px;
    height: 300px;
    cursor: pointer;
}
</style>