<script setup lang="ts">
import { ref } from "vue";
import IconTrash from "~icons/mdi/trash";

const boxes = ref([1, 4, 5]);

const addBox = () => {
  boxes.value.push(0);
};

const increment = (index: number) => {
  if (boxes.value[index] !== undefined) return boxes.value[index]++;
};

const decrement = () => {};
const deleteBox = () => {};
</script>

<template>
  <div class="main">
    <span>Boxes count {{ boxes.length }}</span>
    <span>Marbles count</span>
    <button @click="addBox">Add new box</button>

    <div v-for="(box, index) in boxes" :key="index" class="box">
      <button @click="decrement(index)">-</button>
      <span>{{ box }}</span>
      <button @click="increment(index)">+</button>
      <button class="delete-btn" @click="deleteBox(index)">
        <IconTrash />
      </button>
    </div>
  </div>
</template>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  width: 300px;
  margin: 50px auto;
  align-items: center;
}
.main span {
  font-size: 1.3rem;
}
.delete-btn {
  cursor: pointer;
  border: none;
}
</style>
