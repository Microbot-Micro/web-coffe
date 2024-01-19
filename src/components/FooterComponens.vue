<template>
    <div>
        <section class="footer">

            <div class="share">
                <a href="#" class="fab fa-facebook-f"></a>
                <a href="#" class="fab fa-twitter"></a>
                <a href="#" class="fab fa-instagram"></a>
                <a href="#" class="fab fa-linkedin"></a>
                <a href="#" class="fab fa-pinterest"></a>
            </div>

            <div class="links">
                <a href="#">home</a>
                <a href="#">about</a>
                <a href="#">menu</a>
                <a href="#">products</a>
                <a href="#">review</a>
                <a href="#">contact</a>
                <a href="#">blogs</a>
            </div>

            <div class="credit">2024 Copyright Created by <span @click="goToGitHub">Microbot-Micro</span></div>

        </section>
    </div>
</template>

<script>
export default {
    name: "FooterComponens",
    methods: {
            goToGitHub() {
                window.open('https://github.com/Microbot-Micro/web-coffe', '_blank');
            }
        }
}
</script>

<style lang="scss" scoped></style>

tolong dikasih