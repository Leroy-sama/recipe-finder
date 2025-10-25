<template>
    <header>
        <nav>
            <NuxtLink to="/">
                <NuxtImg src="/assets/images/logo.svg" alt="" />
            </NuxtLink>
            <ul>
                <li>
                    <NuxtLink to="/">Home</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/">Recipes</NuxtLink>
                </li>
            </ul>
            <NuxtLink to="/recipes">Browse Recipes</NuxtLink>
            <div class="burger">
                <NuxtImg src="/assets/images/icon-hamburger-menu.svg" />
            </div>
        </nav>
    </header>
</template>
