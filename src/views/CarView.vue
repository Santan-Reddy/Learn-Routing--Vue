<script setup>
import {useRoute,RouterView,useRouter} from 'vue-router'
import cars from '../data/cars.json'
const route=useRoute()
const router=useRouter()
const carId=parseInt(route.params.id)

const car=cars.find(c=>c.id===carId)

</script>

<template>
    <div v-if="car">
        <h1>Car View</h1>
        <p>{{car.name}}</p>
        <p>{{car.year}}</p>
        <p>{{car.price}}</p>
        <button @click="router.push(`/cars/${carId}/contact`)">Click for contact</button>
        <RouterView/>
    </div>
    <div v-else>Car Not Found</div>
</template>