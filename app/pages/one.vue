<script setup lang="ts">
definePageMeta({
    layout: "recipes",
});
</script>

<template>
    <main>
        <section class="details">
            <div class="wrapper">
                <div class="details-content">
                    <div class="header">
                        <p>
                            Recipes / <span>Mediterranean Chickpea Salad</span>
                        </p>
                    </div>
                    <div class="actual">
                        <div class="iamge">
                            <NuxtImg
                                src="/assets/images/mediterranean-chickpea-salad-large.webp"
                                alt=""
                            />
                        </div>
                        <div class="actual-text">
                            <h2>Mediterranean Chickpea Salad</h2>
                            <p>
                                A refreshing, protein-packed salad tossed in a
                                lemon-olive oil dressing.
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
                            <div class="ingredients">
                                <h3>Ingredients:</h3>
                                <ul>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            1 can (400 g) chickpeas, drained &
                                            rinsed
                                        </p>
                                    </li>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            1 can (400 g) chickpeas, drained &
                                            rinsed
                                        </p>
                                    </li>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            1 can (400 g) chickpeas, drained &
                                            rinsed
                                        </p>
                                    </li>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            1 can (400 g) chickpeas, drained &
                                            rinsed
                                        </p>
                                    </li>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            1 can (400 g) chickpeas, drained &
                                            rinsed
                                        </p>
                                    </li>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            1 can (400 g) chickpeas, drained &
                                            rinsed
                                        </p>
                                    </li>
                                </ul>
                            </div>
                            <div class="ingredients">
                                <h3>Instructions:</h3>
                                <ul>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            In a large bowl combine chickpeas,
                                            cucumber, tomatoes, bell pepper, red
                                            onion and parsley.
                                        </p>
                                    </li>
                                    <li>
                                        <NuxtImg
                                            src="/assets/images/icon-bullet-point.svg"
                                            alt=""
                                        />
                                        <p>
                                            Drizzle with olive oil and lemon
                                            juice.
                                        </p>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- <section class="more">
            <div class="wrapper">
                <div class="more-content">
                    <h2>More Recipes</h2>
                    <div class="more-recipes">
                        <RecipeItem />
                        <RecipeItem />
                    </div>
                </div>
            </div>
        </section> -->
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
