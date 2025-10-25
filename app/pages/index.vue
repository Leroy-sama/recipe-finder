<template>
    <main>
        <section class="hero">
            <div class="wrapper">
                <div class="content">
                    <div class="text-content">
                        <h1>Healthy meals, zero fuss</h1>
                        <p>
                            Discover eight quick, whole-food recipes that you
                            can cook tonight—no processed junk, no guesswork.
                        </p>
                        <NuxtLink to="/recipes">Start exploring</NuxtLink>
                    </div>
                    <div class="image-content">
                        <NuxtImg
                            src="/assets/images/image-home-hero-large.webp"
                        />
                    </div>
                </div>
            </div>
        </section>

        <section class="goodies">
            <div class="wrapper">
                <div class="content">
                    <h2>What you'll get</h2>
                    <div class="goodies-box">
                        <div class="goodie">
                            <NuxtImg src="/public/assets/images/" alt="" />
                            <h3>Whole-food recipes</h3>
                            <p>
                                Each dish uses everyday, unprocessed
                                ingredients.
                            </p>
                        </div>
                        <div class="goodie">
                            <NuxtImg src="/public/assets/images/" alt="" />
                            <h3>Minimum fuss</h3>
                            <p>
                                All recipes are designed to make eating healthy
                                quick and easy.
                            </p>
                        </div>
                        <div class="goodie">
                            <NuxtImg src="/public/assets/images/" alt="" />
                            <h3>Search in seconds</h3>
                            <p>
                                Filter by name or ingredient and jump straight
                                to the recipe you need.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="built">
            <div class="wrapper">
                <div class="content">
                    <div class="built-text">
                        <h2>Built for real life</h2>
                        <div class="paragraphs">
                            <p>
                                Cooking shouldn't be complicated. These recipes
                                come in under 30 minutes of active time, fit
                                busy schedules, and taste good enough to repeat.
                            </p>
                            <p>
                                Whether you're new to the kitchen or just need
                                fresh ideas, we've got you covered.
                            </p>
                        </div>
                    </div>
                    <div class="built-image">
                        <NuxtImg
                            src="/assets/images/image-home-real-life-large.webp"
                        />
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>
