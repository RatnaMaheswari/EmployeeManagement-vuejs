<script setup>
import Employee from './Employee.vue';
    defineProps(['employeesData']);
</script>
<template>
    <div class="employees-container">
        <div class="employee-list">
            <h1>Employees</h1>
            <article v-for='employee in employeesData'>
                <Employee :employee="employee"/>
            <hr />
            </article>
        </div>
    </div>
</template>
<style scoped>

.employees-container {
    display: flex;
    width: 90%;
    margin: 20px auto auto auto;
}
.employee-list{
    width: 100%
}
.employee-list h1 {
    text-align: center;
    margin-bottom: 20px;
    font-weight: bold;
}
</style>