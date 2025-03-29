<template>
  <div class="drawing-container">
    <div class="controls">
      <label for="color">Color:</label>
      <input type="color" v-model="color" />
      
      <label for="size">Size:</label>
      <input type="range" v-model="size" min="1" max="10" />
      
      <button @click="toggleErase">{{ erasing ? 'Stop Erasing' : 'Erase' }}</button>
      <button @click="clearCanvas">Clear</button>
    </div>
    <canvas ref="canvas" width="500" height="400"></canvas>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const canvas = ref(null);
const color = ref('#000000');
const size = ref(3);
const erasing = ref(false);
let drawing = false;
let ctx;

onMounted(() => {
  ctx = canvas.value.getContext('2d');
  canvas.value.addEventListener('mousedown', () => (drawing = true));
  canvas.value.addEventListener('mouseup', () => {
    drawing = false;
    ctx.beginPath();
  });
  canvas.value.addEventListener('mousemove', draw);
});

const draw = (event) => {
  if (!drawing) return;
  ctx.lineWidth = size.value;
  ctx.lineCap = 'round';
  ctx.strokeStyle = erasing.value ? 'white' : color.value;
  
  ctx.lineTo(event.offsetX, event.offsetY);
  ctx.stroke();
  ctx.beginPath();
  ctx.moveTo(event.offsetX, event.offsetY);
};

const toggleErase = () => {
  erasing.value = !erasing.value;
};

const clearCanvas = () => {
  ctx.clearRect(0, 0, canvas.value.width, canvas.value.height);
};
</script>

<style scoped>
.drawing-container { border: 1px solid black; display: inline-block; padding: 10px; }
canvas { cursor: crosshair; display: block; margin: 10px auto; }
.controls { margin-bottom: 10px; }
</style>

