<template>
    <main>
        <section class="mission wrapper">
            <div class="mission-text">
                <span>Our mission</span>
                <h2>Help more people cook nourishing meals, more often.</h2>
                <div class="paragraphs">
                    <p>
                        Healthy Recipe Finder was created to prove that healthy
                        eating can be convenient, affordable, and genuinely
                        delicious.
                    </p>
                    <p>
                        We showcase quick, whole-food dishes that anyone can
                        master—no fancy equipment, no ultra-processed
                        shortcuts—just honest ingredients and straightforward
                        steps.
                    </p>
                </div>
            </div>
            <picture class="image-content">
                <source
                    media="(min-width: 1024px)"
                    srcset="/assets/images/image-about-our-mission-large.webp"
                />
                <img
                    src="/assets/images/image-about-our-mission-small.webp"
                    alt="our-mission image"
                />
            </picture>
        </section>

        <section class="exist wrapper">
            <h2>Why we exist</h2>
            <div class="reasons">
                <div class="reason">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="reason-text">
                        <h3>Cut through the noise.</h3>
                        <p>
                            The internet is bursting with recipes, yet most busy
                            cooks still default to take-away or packaged foods.
                            We curate a tight collection of fool-proof dishes so
                            you can skip the scrolling and start cooking.
                        </p>
                    </div>
                </div>
                <div class="reason">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="reason-text">
                        <h3>Empower home kitchens.</h3>
                        <p>
                            When you control what goes into your meals, you
                            control how you feel. Every recipe is built around
                            unrefined ingredients and ready in about half an
                            hour of active prep.
                        </p>
                    </div>
                </div>
                <div class="reason">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="reason-text">
                        <h3>Make healthy look good.</h3>
                        <p>
                            High-resolution imagery shows you exactly what
                            success looks like—because we eat with our eyes
                            first, and confidence matters.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <section class="philosophy wrapper">
            <h2>Our food philosophy</h2>
            <div class="philos">
                <div class="philo">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="philo-text">
                        <h3>Whole ingredients first.</h3>
                        <p>
                            Fresh produce, grains, legumes, herbs, and quality
                            fats form the backbone of every recipe.
                        </p>
                    </div>
                </div>
                <div class="philo">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="philo-text">
                        <h3>Flavor without compromise.</h3>
                        <p>
                            Spices, citrus, and natural sweetness replace excess
                            salt, sugar, and additives.
                        </p>
                    </div>
                </div>
                <div class="philo">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="philo-text">
                        <h3>Respect for time.</h3>
                        <p>
                            Weeknight meals should slot into real schedules;
                            weekend cooking can be leisurely but never wasteful.
                        </p>
                    </div>
                </div>
                <div class="philo">
                    <NuxtImg
                        src="/assets/images/icon-bullet-point.svg"
                        alt=""
                    />
                    <div class="philo-text">
                        <h3>Sustainable choices.</h3>
                        <p>
                            Short ingredient lists cut down on food waste and
                            carbon footprint, while plant-forward dishes keep
                            things planet-friendly.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <section class="beyond wrapper">
            <div class="beyond-text">
                <h2>Beyond the plate</h2>
                <div class="beyond-words">
                    <p>
                        We believe food is a catalyst for community and
                        well-being. By sharing approachable recipes, we hope to:
                    </p>
                    <ul>
                        <li>Encourage family dinners and social cooking.</li>
                        <li>
                            Reduce reliance on single-use packaging and delivery
                            waste.
                        </li>
                        <li>
                            Spark curiosity about seasonal produce and local
                            agriculture.
                        </li>
                    </ul>
                </div>
            </div>
            <picture class="beyond-image">
                <source
                    media="(min-width: 1024px)"
                    srcset="
                        /assets/images/image-about-beyond-the-plate-large.webp
                    "
                />
                <img
                    src="/assets/images/image-about-beyond-the-plate-small.webp"
                    alt=""
                />
            </picture>
        </section>
    </main>
</template>

<style lang="css" scoped>
.mission {
    padding-block: 3rem;
    display: grid;
    gap: 2.5rem;
}

.mission-text {
    display: grid;
    gap: 1.5rem;
    justify-items: start;
}

.mission-text span {
    background-color: var(--clr-orange-500);
    color: var(--clr-neutral-900);
    padding: 2px 6px;
}

.mission-text h2 {
    color: var(--clr-neutral-900);
    font-size: 2.5rem;
}

.mission-text p {
    color: var(--clr-neutral-600);
    font-size: var(--fs-preset-8);
}

.exist,
.philosophy {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    padding-block: 3rem;
}

.exist h2,
.philosophy h2 {
    color: var(--clr-neutral-900);
    font-size: 2.5rem;
}

.reasons,
.philos {
    display: grid;
    gap: 1.5rem;
}

.reason,
.philo {
    display: flex;
    gap: 1.25rem;
    align-items: start;
}

.reason img,
.philo img {
    max-width: 35px;
}

.reason-text h3,
.philo-text h3 {
    font-size: var(--fs-preset-7);
    color: var(--clr-neutral-900);
}

.reason p,
.philo-text p,
.beyond-text p,
.beyond-text ul li {
    font-size: var(--fs-preset-8);
    color: var(--clr-neutral-600);
}

.beyond {
    padding-block: 3rem;
    display: grid;
    gap: 2rem;
}

.beyond-text {
    display: grid;
    gap: 1.25rem;
}

.beyond-words {
    display: grid;
    gap: 0.75rem;
}

.beyond-text h2 {
    color: var(--clr-neutral-900);
    font-size: 2.5rem;
}
</style>
