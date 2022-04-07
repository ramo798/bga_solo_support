<script setup lang="ts">
import { ref } from "vue";
const blue = ref<Array<Number>>([]);
const red = ref<Array<Number>>([]);
const ye = ref<Array<Number>>([]);
const gree = ref<Array<Number>>([]);
const joker = ref<Array<Number>>([]);
for (var i = 0; i < 13; i++) blue.value.push(0);
for (var i = 0; i < 13; i++) red.value.push(0);
for (var i = 0; i < 13; i++) ye.value.push(0);
for (var i = 0; i < 13; i++) gree.value.push(0);
for (var i = 0; i < 3; i++) joker.value.push(0);
</script>

<template>
  <div>
    <p>スキップ 2枚</p>
    <p>ドロー2 2枚</p>
    <p>リバース 2枚</p>
    <p>スワップ 1枚</p>
    <div style="display: flex; justify-content: space-between">
      <div>
        <div v-for="(value, index) in blue" style="margin-top: 30px">
          <button v-if="index < 9" @click="blue[index] = blue[index].valueOf() + 1">B{{ index + 1 }}---{{ value }}</button>
          <button v-else-if="index == 9" @click="blue[index] = blue[index].valueOf() + 1">Bスキップ---{{ value }}</button>
          <button v-else-if="index == 10" @click="blue[index] = blue[index].valueOf() + 1">Bドロー2---{{ value }}</button>
          <button v-else-if="index == 11" @click="blue[index] = blue[index].valueOf() + 1">Bリバース---{{ value }}</button>
          <button v-else-if="index == 12" @click="blue[index] = blue[index].valueOf() + 1">Bスワップ---{{ value }}</button>
        </div>
      </div>
      <div>
        <div v-for="(value, index) in red" style="margin-top: 30px">
          <button v-if="index < 9" @click="red[index] = red[index].valueOf() + 1">R{{ index + 1 }}---{{ value }}</button>
          <button v-else-if="index == 9" @click="red[index] = red[index].valueOf() + 1">Rスキップ---{{ value }}</button>
          <button v-else-if="index == 10" @click="red[index] = red[index].valueOf() + 1">Rドロー2---{{ value }}</button>
          <button v-else-if="index == 11" @click="red[index] = red[index].valueOf() + 1">Rリバース---{{ value }}</button>
          <button v-else-if="index == 12" @click="red[index] = red[index].valueOf() + 1">Rスワップ---{{ value }}</button>
        </div>
      </div>
      <div>
        <div v-for="(value, index) in ye" style="margin-top: 30px">
          <button v-if="index < 9" @click="ye[index] = ye[index].valueOf() + 1">Y{{ index + 1 }}---{{ value }}</button>
          <button v-else-if="index == 9" @click="ye[index] = ye[index].valueOf() + 1">Yスキップ---{{ value }}</button>
          <button v-else-if="index == 10" @click="ye[index] = ye[index].valueOf() + 1">Yドロー2---{{ value }}</button>
          <button v-else-if="index == 11" @click="ye[index] = ye[index].valueOf() + 1">Yリバース---{{ value }}</button>
          <button v-else-if="index == 12" @click="ye[index] = ye[index].valueOf() + 1">Yスワップ---{{ value }}</button>
        </div>
      </div>
      <div>
        <div v-for="(value, index) in gree" style="margin-top: 30px">
          <button v-if="index < 9" @click="gree[index] = gree[index].valueOf() + 1">G{{ index + 1 }}---{{ value }}</button>
          <button v-else-if="index == 9" @click="gree[index] = gree[index].valueOf() + 1">Gスキップ---{{ value }}</button>
          <button v-else-if="index == 10" @click="gree[index] = gree[index].valueOf() + 1">Gドロー2---{{ value }}</button>
          <button v v-else-if="index == 11" @click="gree[index] = gree[index].valueOf() + 1">Gリバース---{{ value }}</button>
          <button v-else-if="index == 12" @click="gree[index] = gree[index].valueOf() + 1">Gスワップ---{{ value }}</button>
        </div>
      </div>
      <div>
        <div>
          <button @click="joker[0] = joker[0].valueOf() + 1" style="margin-top: 30px">四色---{{ joker[0] }}</button>
        </div>
        <div>
          <button @click="joker[1] = joker[1].valueOf() + 1" style="margin-top: 30px">ドロー4---{{ joker[1] }}</button>
        </div>
        <div>
          <button @click="joker[2] = joker[2].valueOf() + 1" style="margin-top: 30px">スワップ---{{ joker[2] }}</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
