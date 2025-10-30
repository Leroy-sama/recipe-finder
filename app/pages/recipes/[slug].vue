<script setup lang="ts">
definePageMeta({
    layout: "recipes",
});

import { type Recipe } from "~~/types/recipe";

const { slug } = useRoute().params;
const { data: recipes } = await useFetch<Recipe[]>("/data.json");
const recipe = recipes.value?.find((rec) => rec.slug === slug);
const otherRecipes = recipes.value?.filter((rec) => rec.slug !== slug);
console.log(otherRecipes);
</script>

<template>
    <main>
        <section class="details">
            <div class="wrapper">
                <div class="details-content">
                    <div class="header">
                        <p>
                            Recipes / <span>{{ recipe?.title }}</span>
                        </p>
                    </div>
                    <div class="actual">
                        <div class="iamge">
                            <NuxtImg
                                :src="recipe?.image.large"
                                :alt="recipe?.title"
                            />
                        </div>
                        <div class="actual-text">
                            <h2>{{ recipe?.title }}</h2>
                            <p>
                                {{ recipe?.overview }}
                            </p>
                            <div class="metrics">
                                <div class="metric">
                                    <NuxtImg
                                        src="/assets/images/icon-servings.svg"
                                        alt=""
                                    />
                                    <span
                                        >Servings: {{ recipe?.servings }}</span
                                    >
                                </div>
                                <div class="metric">
                                    <NuxtImg
                                        src="/assets/images/icon-prep-time.svg"
                                        alt=""
                                    />
                                    <span
                                        >Prep:
                                        {{ recipe?.prepMinutes }} mins</span
                                    >
                                </div>
                                <div class="metric">
                                    <NuxtImg
                                        src="/assets/images/icon-cook-time.svg"
                                        alt=""
                                    />
                                    <span
                                        >Cook:
                                        {{ recipe?.cookMinutes }} mins</span
                                    >
                                </div>
                            </div>
                            <div class="ingredients">
                                <h3>Ingredients:</h3>
                                <ul v-for="ingredient in recipe?.ingredients">
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            {{ ingredient }}
                                        </p>
                                    </li>
                                </ul>
                            </div>
                            <div class="ingredients">
                                <h3>Instructions:</h3>
                                <ul v-for="instruction in recipe?.instructions">
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            {{ instruction }}
                                        </p>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="more">
            <div class="wrapper">
                <div class="more-content">
                    <h2>More Recipes</h2>
                    <div
                        class="more-recipes"
                        v-for="recipe in otherRecipes?.slice(0, 3)"
                    >
                        <RecipeItem :recipe="recipe" />
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="css" scoped>
.details {
    padding-block: 3rem;
}

.details-content {
    display: grid;
    gap: 1rem;
}

.header p {
    color: var(--clr-neutral-600);
}

.header p span {
    color: var(--clr-neutral-900);
}

.actual {
    display: grid;
    gap: 2.5rem;
}

.actual-text {
    display: grid;
    gap: 1.25rem;
}

.actual-text h2 {
    color: var(--clr-neutral-900);
    font-size: var(--fs-preset-5);
}

.actual-text p {
    font-size: var(--fs-preset-9);
    color: var(--clr-neutral-600);
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

.ingredients {
    display: grid;
    gap: 1rem;
}

.ingredients h3 {
    font-size: var(--fs-preset-7);
    color: var(--clr-neutral-900);
}

.ingredients li {
    display: flex;
    align-items: center;
    gap: 0.5rem;

    img {
        max-width: 24px;
    }
}

.more {
    padding-block: 3rem;
}

.more-content {
    display: grid;
    gap: 1.5rem;
}

.more-content h2 {
    color: var(--clr-neutral-900);
    font-size: var(--fs-preset-6);
}

.more-recipes {
    display: grid;
    gap: 2rem;
}
</style>
