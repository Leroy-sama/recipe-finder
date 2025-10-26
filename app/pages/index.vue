<template>
    <main>
        <section class="hero">
            <div class="wrapper">
                <div class="hero-content">
                    <div class="text-content">
                        <div class="headings">
                            <h1>Healthy meals, zero fuss</h1>
                            <p>
                                Discover eight quick, whole-food recipes that
                                you can cook tonight—no processed junk, no
                                guesswork.
                            </p>
                        </div>
                        <NuxtLink to="/recipes" class="hero-btn"
                            >Start exploring</NuxtLink
                        >
                    </div>
                    <picture class="image-content">
                        <source
                            srcset="/assets/images/image-home-hero-large.webp"
                            media="(min-width: 1024px)"
                        />
                        <img
                            src="/assets/images/image-home-hero-small.webp"
                            alt="home hero image"
                        />
                    </picture>
                </div>
            </div>
        </section>

        <section class="goodies">
            <div class="wrapper">
                <div class="goodies-content">
                    <h2>What you'll get</h2>
                    <div class="goodies-box">
                        <div class="goodie">
                            <div class="goodie-img">
                                <NuxtImg
                                    src="/assets/images/icon-whole-food-recipes.svg"
                                    alt=""
                                />
                            </div>
                            <div class="goodie-text">
                                <h3>Whole-food recipes</h3>
                                <p>
                                    Each dish uses everyday, unprocessed
                                    ingredients.
                                </p>
                            </div>
                        </div>
                        <div class="goodie">
                            <div class="goodie-img">
                                <NuxtImg
                                    src="/assets/images/icon-minimum-fuss.svg"
                                    alt=""
                                />
                            </div>
                            <div class="goodie-text">
                                <h3>Minimum fuss</h3>
                                <p>
                                    All recipes are designed to make eating
                                    healthy quick and easy.
                                </p>
                            </div>
                        </div>
                        <div class="goodie">
                            <div class="goodie-img">
                                <NuxtImg
                                    src="/assets/images/icon-search-in-seconds.svg"
                                    alt=""
                                />
                            </div>
                            <div class="goodie-text">
                                <h3>Search in seconds</h3>
                                <p>
                                    Filter by name or ingredient and jump
                                    straight to the recipe you need.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="built">
            <div class="wrapper">
                <div class="built-content">
                    <div class="built-text">
                        <h2>Built for real life</h2>

                        <p>
                            Cooking shouldn't be complicated. These recipes come
                            in under 30 minutes of active time, fit busy
                            schedules, and taste good enough to repeat.
                        </p>
                        <p>
                            Whether you're new to the kitchen or just need fresh
                            ideas, we've got you covered.
                        </p>
                    </div>
                    <picture class="built-image">
                        <source
                            media="(min-width: 1024px)"
                            srcset="
                                /assets/images/image-home-real-life-large.webp
                            "
                        />
                        <img
                            src="/assets/images/image-home-real-life-small.webp"
                            alt="built for real life image"
                        />
                    </picture>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="css" scoped>
.hero {
    padding-top: 3rem;
    padding-bottom: 4rem;

    @media (min-width: 768px) {
        padding-bottom: 5rem;
    }

    @media (min-width: 1024px) {
        padding-top: 5rem;
        padding-bottom: 6rem;
    }
}

.hero-content {
    display: grid;
    gap: 2.5rem;

    @media (min-width: 1024px) {
        gap: 5rem;
    }
}

.text-content {
    display: grid;
    gap: 2rem;
    justify-items: center;

    @media (min-width: 1024px) {
        gap: 2.5rem;
    }
}

.headings {
    display: grid;
    gap: 1rem;

    @media (min-width: 1024px) {
        gap: 0.75rem;
    }
}

.headings h1 {
    color: var(--clr-neutral-900);
    font-size: var(--fs-preset-3);

    @media (min-width: 768px) {
        font-size: var(--fs-preset-2);
    }

    @media (min-width: 1024px) {
        font-size: var(--fs-preset-1);
    }
}

.headings p {
    color: var(--clr-neutral-600);
    font-size: var(--fs-preset-8);
}

.hero-btn {
    padding: 1rem 2rem;
    background-color: var(--clr-neutral-900);
    color: var(--clr-white);
}

.image-content {
    border-radius: 8px;
    padding: 8px;
    background-color: var(--clr-white);
}

.goodies-content {
    display: grid;
    gap: 2rem;
}

.goodies-content h2 {
    color: var(--clr-neutral-900);
}

.goodies-box {
    display: grid;
    gap: 1.5rem;

    @media (min-width: 768px) {
        gap: 2rem;
    }

    @media (min-width: 1024px) {
        grid-template-columns: repeat(3, 1fr);
    }
}

.goodie {
    display: grid;
    gap: 1.5rem;
}

.goodie-img {
    width: 60px;
    height: 60px;
    background-color: var(--clr-white);
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.goodie-img img {
    max-width: 40px;
}

.goodie-text {
    display: grid;
    gap: 0.75rem;
}

.goodie-text h3 {
    color: var(--clr-neutral-900);
}

.goodie-text p {
    color: var(--clr-neutral-600);
}

.built {
    padding-block: 4rem;

    @media (min-width: 768px) {
        padding-block: 5rem;
    }
    @media (min-width: 1024px) {
        padding-block: 6rem;
    }
}

.built-content {
    display: grid;
    gap: 2rem;

    @media (min-width: 768px) {
        gap: 2.5rem;
    }

    @media (min-width: 1024px) {
        gap: 3rem;
        grid-template-columns: repeat(2, 1fr);
        align-items: center;
    }
}

.built-text {
    display: grid;
    gap: 1.25rem;
}

.built-text h2 {
    color: var(--clr-neutral-900);
    font-size: 3rem;
}

.built-text p {
    font-size: var(--fs-preset-9);
    color: var(--clr-neutral-600);
}
</style>
