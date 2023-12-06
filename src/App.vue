<script setup>
import { ref, onMounted } from 'vue';
import Employees from './components/Employees.vue';
import Navbar from './components/Navbar.vue';
  const employeesList = ref([]);
onMounted(() => {
  fetch('https://employeemanagementsystem-5d5u.onrender.com/api')
    .then(response => response.json())
    .then(res => employeesList.value = res)
})
</script>

<template>
  <div>
    <Navbar />
  <main>
    <div class="main-container">
      <Employees :employeesData="employeesList" />
    </div>
  </main>
  </div>
  
</template>

<style scoped>
</style>
