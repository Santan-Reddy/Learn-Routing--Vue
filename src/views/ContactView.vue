<script setup>
import {useRoute,useRouter} from 'vue-router'
import cars from '../data/cars.json'
const route=useRoute()
const carId=parseInt(route.params.id)
const car=cars.find(c=>c.id===carId)

</script>

<template>
    <div v-if="car">
        <h1>Contact Info</h1>
        <p>{{ car.contact.dealer }} </p>
        <p>{{ car.contact.number }} </p>
    </div>
</template>