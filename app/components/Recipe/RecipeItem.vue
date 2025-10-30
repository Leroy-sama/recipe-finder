<script setup lang="ts">
import { type Recipe } from "~~/types/recipe";

defineProps<{
    recipe: Recipe;
}>();
</script>

<template>
    <div class="recipe">
        <picture>
            <source media="(min-width: 1024px)" :src="recipe.image.large" />
            <img :src="recipe.image.small" :alt="recipe.title" />
        </picture>
        <div class="recipe-info">
            <div class="info-text">
                <h3>{{ recipe.title }}</h3>
                <p>
                    {{ recipe.overview }}
                </p>
            </div>
            <div class="metrics">
                <div class="metric">
                    <NuxtImg src="/assets/images/icon-servings.svg" alt="" />
                    <span>Servings: {{ recipe.servings }}</span>
                </div>
                <div class="metric">
                    <NuxtImg src="/assets/images/icon-prep-time.svg" alt="" />
                    <span>Prep: {{ recipe.prepMinutes }} mins</span>
                </div>
                <div class="metric">
                    <NuxtImg src="/assets/images/icon-cook-time.svg" alt="" />
                    <span>Cook: {{ recipe.cookMinutes }} mins</span>
                </div>
            </div>
        </div>
        <NuxtLink class="recipe-btn" :to="`/recipes/${recipe.slug}`"
            >View Recipe</NuxtLink
        >
    </div>
</template>

<style lang="css" scoped>
.recipe-info {
    display: grid;
    gap: 1rem;
}

.info-text {
    display: grid;
    gap: 0.625rem;
}

.recipe-info h3 {
    font-size: 1.25rem;
    color: var(--clr-neutral-900);
}

.recipe-info p {
    font-size: 1rem;
    color: var(--clr-neutral-600);
}

.recipe {
    background-color: var(--clr-white);
    padding: 0.5rem;
    display: grid;
    gap: 1rem;
}

.metrics {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
}

.metric {
    display: flex;
    gap: 6px;
    white-space: nowrap;
}

.metric span {
    color: var(--clr-neutral-900);
}

.metric img {
    max-width: 20px;
}

.recipe-btn {
    color: var(--clr-white);
    background-color: var(--clr-neutral-900);
    padding: 0.75rem 2rem;
    display: flex;
    justify-content: center;
    border-radius: var(--radius-full);
}
</style>
