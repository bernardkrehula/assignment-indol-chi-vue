<script setup lang="ts">
import IconTrash from "~icons/mdi/trash";
</script>

<template>
  <div class="main">
    <button class="delete-btn">
      <IconTrash />
    </button>
  </div>
</template>

<style scoped>
.main {
  width: 300px;
  margin: 100px auto;
  background-color: gray;
}
.delete-btn{
  cursor: pointer;
  border: none;
}
</style>
