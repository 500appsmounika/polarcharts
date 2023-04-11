<template>
    <polarchart :data="chartData" />
  </template>
  
  <script setup>
 //define the give data
       const chartData={
          labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple'],
          datasets: [
            {
              label: '# of Votes',
              data: [12, 19, 3, 5, 2],
              backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
              ],
              borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(15, 10, 25, 1)',
              ],
              borderWidth: 1,
            },
          ],
        }
     
  </script>