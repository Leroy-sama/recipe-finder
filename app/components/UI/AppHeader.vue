<script setup lang="ts">
const state = reactive({
    isActive: false,
});

const toggleNavMenu = () => {
    state.isActive = !state.isActive;
};

const closeNavMenu = () => {
    state.isActive = false;
};
</script>

<template>
    <header>
        <nav>
            <NuxtLink to="/" class="logo">
                <NuxtImg src="/assets/images/logo.svg" alt="logo svg" />
            </NuxtLink>
            <ul :class="{ active: state.isActive }">
                <li>
                    <NuxtLink to="/" @click.native="closeNavMenu"
                        >Home</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink to="/about" @click.native="closeNavMenu"
                        >About</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink to="/recipes" @click.native="closeNavMenu"
                        >Recipes</NuxtLink
                    >
                </li>
                <li class="special">
                    <NuxtLink to="/" class="mobi" @click.native="closeNavMenu"
                        >Browse Recipes</NuxtLink
                    >
                </li>
            </ul>
            <NuxtLink to="/recipes" class="cta-btn desk"
                >Browse Recipes</NuxtLink
            >
            <div
                class="burger mobi"
                @click="toggleNavMenu"
                :class="{ active: state.isActive }"
            >
                <NuxtImg src="/assets/images/icon-hamburger-menu.svg" />
            </div>
        </nav>
    </header>
</template>

<style lang="css" scoped>
header {
    padding: 2rem;
    padding-bottom: 20px;
    border-bottom: 1px solid var(--clr-neutral-300);
}
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo img {
    max-width: 260px;
}

ul {
    list-style: none;
    position: fixed;
    inset: 4rem 5% 70% 5%;
    background-color: var(--clr-white);
    border: 1px solid red;
    border-radius: 8px;
    padding: 8px;
    display: flex;
    flex-direction: column;
    gap: 0.25rem;
    transform: translateX(110%);
    transition: all 0.2s ease;

    &.active {
        transform: translateX(0%);
    }

    li a {
        color: var(--clr-neutral-900);
        padding: 8px;
    }

    li {
        width: 100%;
    }

    .special a {
        background-color: var(--clr-neutral-900);
        color: var(--clr-white);
        white-space: nowrap;
        padding: 0.75rem 1rem;
        width: 100%;
    }

    @media (min-width: 1024px) {
        position: static;
        inset: 0;
        flex-direction: row;
        background-color: var(--clr-neutral-100);
        transform: translateX(0%);
    }
}

.cta-btn {
    background-color: var(--clr-neutral-900);
    color: var(--clr-white);
    white-space: nowrap;
    padding: 0.75rem 1rem;
}
</style>
