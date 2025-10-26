<template>
    <NuxtLayout>
        <NuxtPage />
    </NuxtLayout>
</template>

<style lang="css">
@font-face {
    font-family: "Nunito";
    src: url(/assets/fonts/Nunito/Nunito-VariableFont_wght.ttf)
        format("truetype");
    font-weight: 400;
}

@font-face {
    font-family: "Nunito Sans";
    src: url(/assets/fonts/Nunito_Sans/NunitoSans-VariableFont_YTLC\,opsz\,wdth\,wght.ttf)
        format("truetype");
    font-weight: 400;
}

:root {
    --clr-neutral-900: #163a34;
    --clr-neutral-600: #395852;
    --clr-neutral-300: #d0dcd9;
    --clr-neutral-200: #e0e6e3;
    --clr-neutral-100: #f6f5f1;
    --clr-white: #ffffff;
    --clr-orange-500: #fe9f6b;
    --clr-teal-500: #49ac9b;
    --clr-indigo-500: #697ddb;

    --ff-primary: "Nunito", system-ui;
    --ff-secondary: "Nunito Sans", system-ui;

    --fs-preset-1: 4.5rem;
    --fs-preset-2: 4rem;
    --fs-preset-3: 3.25rem;
    --fs-preset-4: 3rem;
    --fs-preset-5: 2.5rem;
    --fs-preset-6: 2rem;
    --fs-preset-7: 1.5rem;
    --fs-preset-8: 1.25rem;
    --fs-preset-9: 1.125rem;
    --fs-preset-10: 1rem;
    --fs-preset-11: 0.875rem;

    --spacing-0: 0;
    --spacing-025: 2px;
    --spacing-050: 4px;
    --spacing-075: 6px;
    --spacing-100: 8px;
    --spacing-125: 10px;
    --spacing-150: 12px;
    --spacing-200: 16px;
    --spacing-250: 20px;
    --spacing-300: 24px;
    --spacing-400: 32px;
    --spacing-500: 40px;
    --spacing-600: 48px;
    --spacing-800: 64px;
    --spacing-1000: 80px;
    --spacing-1200: 96px;
    --spacing-1400: 112px;
    --spacing-1600: 128px;
    --spacing-1800: 140px;

    --radius-0: 0;
    --radius-4: 4px;
    --radius-6: 6px;
    --radius-8: 8px;
    --radius-10: 10px;
    --radius-12: 12px;
    --radius-16: 16px;
    --radius-20: 20px;
    --radius-24: 24px;
    --radius-full: 999px;
}

*,
*::before,
*::after {
    box-sizing: border-box;
}

* {
    margin: 0;
}

body {
    font-family: var(--ff-primary);
    background-color: var(--clr-neutral-100);
}

img,
picture,
video,
svg {
    display: block;
    width: 100%;
}

input,
button,
textarea,
select {
    font: inherit;
}

p,
h1,
h2,
h3,
h4,
h5,
h6 {
    overflow-wrap: break-word;
}

p {
    text-wrap: pretty;
    line-height: 1.6;
}
h1,
h2,
h3,
h4,
h5,
h6 {
    text-wrap: balance;
    line-height: 1.1;
}

a {
    text-decoration: none;
    transition: all 0.2s ease-in-out;
}

ul {
    padding: 0;
}

#root,
#__next {
    isolation: isolate;
}

.wrapper {
    width: min(74.5rem, 90%);
    margin-inline: auto;
}

.desk {
    display: none;

    @media (min-width: 1024px) {
        display: block;
    }
}

.mobi {
    display: block;

    @media (min-width: 1024px) {
        display: none;
    }
}
</style>
