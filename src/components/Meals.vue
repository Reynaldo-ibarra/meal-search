<script setup>
import MealItem from './MealItem.vue';

const { meals } = defineProps({
    meals: {
        type: Array,
        required: true
    }
})
</script>

<template>
    <div class="grid grid-cols-3 gap-5 p-8">
        <MealItem v-for="meal in meals" :key="meal.idMeal" :meal="meal" />
    </div>

    <div v-if="!meals || !meals.length" class="flex justify-center text-gray-600">
        Meals Not Found
    </div>
</template>
