<script setup>
import RecipeCardImage from './RecipeCardImage.vue'
import RecipeCardQuickview from './RecipeCardQuickview.vue'
import { ref } from 'vue'
defineProps(['recipe'])

const isImage = ref(true)
</script>

<template>
<section class="recipe-card">
    <!-- <RecipeCardImage v-if="isImage" @click="isImage=false" :recipe/>
    <RecipeCardQuickview v-else v-on:to-image="isImage=true" :isImage :recipe/> -->
    <component 
      :is="isImage ? RecipeCardImage : RecipeCardQuickview"
      :recipe
      @to-image="isImage=true"
      @to-quickview="isImage=false"

    />
  </section>
</template>

<style scoped>
/* RECIPE CARD STYLES */
.recipe-card {
  width:100%;
  display:flex;
  flex-direction:column;
  border-radius:10px;
  box-shadow: 0 0 5px #ddd;
  padding:15px;
  text-align: center;
}
/* ----------------- */









</style>