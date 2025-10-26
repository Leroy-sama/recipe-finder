<template>
    <section class="cta wrapper">
        <div class="cta-text">
            <h2>Ready to cook smarter?</h2>
            <p>
                Hit the button, pick a recipe, and get dinner on the table—fast.
            </p>
        </div>
        <NuxtLink to="/recipes">Browse recipes </NuxtLink>
    </section>
</template>

<style lang="css" scoped>
.cta {
    background-color: var(--clr-neutral-200);
    padding-block: 3rem;
    display: grid;
    justify-items: center;
    gap: 2rem;

    @media (min-width: 768px) {
        padding-block: 5rem;
        gap: 2.5rem;
    }

    @media (min-width: 1024px) {
        padding-block: 6rem;
    }
}

.cta-text {
    display: grid;
    gap: 0.75rem;
}

h2 {
    color: var(--clr-neutral-900);
    font-size: var(--fs-preset-5);

    @media (min-width: 768px) {
        font-size: var(--fs-preset-4);
    }
}

p {
    font-size: var(--fs-preset-9);
    color: var(--clr-neutral-600);
}

a {
    padding: 1rem 2rem;
    background-color: var(--clr-neutral-900);
    color: var(--clr-white);
}
</style>
