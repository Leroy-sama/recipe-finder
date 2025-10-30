<script setup lang="ts">
definePageMeta({
    layout: "recipes",
});

import { type Recipe } from "~~/types/recipe";

const { data: recipes } = await useFetch<Recipe[]>("/data.json");
</script>

<template>
    <main>
        <header>
            <h2>Explore our simple, healthy recipes</h2>
            <p>
                Discover eight quick, whole-food dishes that fit real-life
                schedules and taste amazing. Use the search bar to find a recipe
                by name or ingredient, or simply scroll the list and let
                something delicious catch your eye.
            </p>
        </header>

        <section class="recipes">
            <div class="wrapper">
                <div class="recipes-content">
                    <div class="header">
                        <div class="selectss">
                            <select name="prep" id="prep">
                                <option value="" disabled selected>
                                    Max Prep Time
                                </option>
                                <option value="0">0 minutes</option>
                                <option value="5">5 minutes</option>
                                <option value="10">10 minutes</option>
                                <!-- <button>Clear</button> -->
                            </select>

                            <select name="cook" id="cook">
                                <option value="" disabled selected>
                                    Max Cook Time
                                </option>
                                <option value="0">0 minutes</option>
                                <option value="5">5 minutes</option>
                                <option value="10">10 minutes</option>
                                <option value="15">15 minutes</option>
                                <option value="20">20 minutes</option>
                                <!-- <button>Clear</button> -->
                            </select>
                        </div>
                        <div class="form">
                            <NuxtImg
                                src="/assets/images/icon-search.svg"
                                alt=""
                            />
                            <input
                                type="text"
                                placeholder="Search by name or ingredient..."
                            />
                        </div>
                    </div>
                    <div class="recipes-box">
                        <RecipeItem
                            v-for="recipe in recipes"
                            :recipe="recipe"
                        />
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="css" scoped>
header {
    padding-block: 3rem;
    display: grid;
    gap: 0.75rem;
}

header h2 {
    color: var(--clr-neutral-900);
    font-size: 2.5rem;
}

header p {
    color: var(--clr-neutral-600);
}

.header {
    display: grid;
    gap: 0.75rem;
}

.selectss {
    display: grid;
    gap: 0.75rem;
}

.selectss select {
    padding: 1rem 10px;
    border-radius: 10px;
    background-color: var(--clr-white);
}

.form {
    display: flex;
    align-items: center;
    background-color: var(--clr-white);
    gap: 0.75rem;
    padding: 1rem 10px;
    border: 1px solid var(--clr-neutral-300);
    border-radius: 10px;
}

.form img {
    width: 20px;
    height: 20px;
}

.form input {
    border: none;
    outline: none;
}

.recipes-box {
    display: grid;
    gap: 2rem;

    @media (min-width: 1024px) {
        grid-template-columns: repeat(3, 1fr);
    }
}
</style>
