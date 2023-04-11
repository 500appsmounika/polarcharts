<template>
    <!--accesing the data in ref-->
    <canvas ref="canvasRef"></canvas>
  </template>
  
  <script setup>
  import { onMounted, onUnmounted, ref } from 'vue';
  import Chart from 'chart.js/auto';
  //define the props
  const props = defineProps({
    data: {
      type: Object,
      required: true,
    },
  });
  //initialize the ref 
  const canvasRef = ref(null);
  let chartInstance = null;
  //show the polar chart
  onMounted(() => {
    const canvas = canvasRef.value;
    chartInstance = new Chart(canvas, {
      type: 'polarArea',
      data: props.data,
    });
  });
  
  onUnmounted(() => {
    chartInstance.destroy();
  });
  </script>