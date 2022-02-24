<template>
  <div class="flex">
      <cat :image="cat.image" @click="increment()" />

      <div class="text-center">
        <h2>Veces pulsado:</h2>
        <h3>{{ cat.counter }}</h3>    
      </div>
      
  </div>
</template>

<script>
import cat from './cat.vue'
export default {
  components: { cat },
    name:'Counter',
    props: {
        cat: {
            type: Object,
            require: true
        }
    },
    methods: {
    increment(){
        this.$emit('event-increment');
    }
  }

}
</script>

<style scoped>
.flex{
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.text-center{
    text-align: center;
}
</style>