<template>
    <div class="ingredient-list">
        <span v-for="ingredient in ingredients" :key="ingredient">
            {{ ingredient }}
            <button @click="removeIngredient(ingredient)">x</button>
        </span>
    </div>
</template>
  
<script>
export default {
    props: ['ingredients'],
    methods: {
        removeIngredient(ingredient) {
            this.$emit('remove-ingredient', ingredient);
        },
    }
}
</script>
  
<style scoped>
.ingredient-list span {
    margin: 5px;
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
}
</style>