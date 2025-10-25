<script setup lang="ts">
definePageMeta({
    layout: "recipes",
});
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
                            <NuxtImg
                                src="/assets/images/icon-chevron-down.svg"
                                alt=""
                            />
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
                        <div class="recipe">
                            <NuxtImg
                                src="/assets/images/mediterranean-chickpea-salad-large.webp"
                                alt=""
                            />
                            <div class="recipe-info">
                                <h3>Mediterranean Chickpea Salad Large</h3>
                                <p>
                                    A refreshing, protein packed salad tossed in
                                    a lemon-olive oil dressing.
                                </p>
                                <div class="metrics">
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-servings.svg"
                                            alt=""
                                        />
                                        <span>Servings: 2</span>
                                    </div>
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-prep-time.svg"
                                            alt=""
                                        />
                                        <span>Prep: 10 mins</span>
                                    </div>
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-cook-time.svg"
                                            alt=""
                                        />
                                        <span>Cook: 0 mins</span>
                                    </div>
                                </div>
                            </div>
                            <NuxtLink to="/recipes">View Recipe</NuxtLink>
                        </div>
                        <div class="recipe">
                            <NuxtImg
                                src="/assets/images/mediterranean-chickpea-salad-large.webp"
                                alt=""
                            />
                            <div class="recipe-info">
                                <h3>Mediterranean Chickpea Salad Large</h3>
                                <p>
                                    A refreshing, protein packed salad tossed in
                                    a lemon-olive oil dressing.
                                </p>
                                <div class="metrics">
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-servings.svg"
                                            alt=""
                                        />
                                        <span>Servings: 2</span>
                                    </div>
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-prep-time.svg"
                                            alt=""
                                        />
                                        <span>Prep: 10 mins</span>
                                    </div>
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-cook-time.svg"
                                            alt=""
                                        />
                                        <span>Cook: 0 mins</span>
                                    </div>
                                </div>
                            </div>
                            <NuxtLink to="/recipes">View Recipe</NuxtLink>
                        </div>
                        <div class="recipe">
                            <NuxtImg
                                src="/assets/images/mediterranean-chickpea-salad-large.webp"
                                alt=""
                            />
                            <div class="recipe-info">
                                <h3>Mediterranean Chickpea Salad Large</h3>
                                <p>
                                    A refreshing, protein packed salad tossed in
                                    a lemon-olive oil dressing.
                                </p>
                                <div class="metrics">
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-servings.svg"
                                            alt=""
                                        />
                                        <span>Servings: 2</span>
                                    </div>
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-prep-time.svg"
                                            alt=""
                                        />
                                        <span>Prep: 10 mins</span>
                                    </div>
                                    <div class="metric">
                                        <NuxtImg
                                            src="/assets/images/icon-cook-time.svg"
                                            alt=""
                                        />
                                        <span>Cook: 0 mins</span>
                                    </div>
                                </div>
                            </div>
                            <NuxtLink to="/recipes">View Recipe</NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        Max Prep Time Max Cook Time Search by name or ingredient...

        <!-- Populate recipes using data from the data.json file -->

        Made with ❤️ and 🥑
    </main>
</template>
