<script setup>
import cars from '../data/cars.json'
import {RouterLink} from 'vue-router'
 </script>
<template>
    <div>
        <h1>Home View</h1>
        <div class="cars">
            <RouterLink :to="`/cars/${car.id}`" v-for="car in cars" :key="car.id">
                {{ car.name }}
            </RouterLink>
        </div>
    </div>
</template>

<style scoped>
.cars{
    display: flex;
    gap: 1rem;
}
.cars a{
    text-decoration: none;
    color: blue;
    border: 2px solid black;
}
</style>