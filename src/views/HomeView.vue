

<template>
  <div class="home">
    <div class="count">
      {{ count }}
    </div>
    <div class="buttons">
      <button @click="decreaseCount">-</button>
      <button @click="increaseCount">+</button>
      <hr>
      <br/>
      <div>
        This counter is: {{ oddOrEven }}
      </div>

    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
const count = ref(0);
const increaseCount = () => {
  count.value++;
}
const decreaseCount = () => {
  count.value--;
}
const oddOrEven = computed(() =>{
  return count.value % 2 === 0 ? 'even' : 'odd'
})
 

</script>

<style>
.count{
  font-size: 70px;
  margin: 30px;
}
.buttons button {
  font-size: 50px;
  margin: 20px;
}

</style>
