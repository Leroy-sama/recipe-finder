<template>
    <footer>
        <div class="wrapper">
            <div class="footer-content">
                <p>Made with ❤️ and 🥑</p>
                <div class="links">
                    <a href="#">
                        <NuxtImg src="/assets/images/icon-instagram.svg" />
                    </a>
                    <a href="#">
                        <NuxtImg src="/assets/images/icon-bluesky.svg" />
                    </a>
                    <a href="#">
                        <NuxtImg src="/assets/images/icon-tiktok.svg" />
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="css" scoped>
footer {
    padding-block: 2.5rem;
}

.footer-content {
    display: flex;
    justify-content: space-between;
}

.links {
    display: flex;
    gap: 1.5rem;
}
</style>
