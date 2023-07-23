<script setup>
import { ref } from "vue"
const cells = ref([
  [null, null, null],
  [null, null, null],
  [null, null, null]
])
</script>

<template>
  <div class="content">
    <div class="count">
      0 : 0
    </div>
    <div class="row" v-for="row in cells">
      <div class="cell" v-for="cell in row">
        <img src="./assets/img/cross.png">
        <img src="./assets/img/star.png">
      </div>
    </div>
  </div>
</template>

<style>
.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
}

.count {
  font-size: 40px;
  font-weight: bold;
  margin-bottom: 30px;
  color: rgb(112, 112, 112);
}

.row {
  display: flex;
  gap: 10px;
  margin-bottom: 10px;
}

.cell {
  width: 240px;
  height: 240px;
  background: #DDDDDD;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
