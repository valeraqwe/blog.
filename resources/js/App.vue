<template>
    <div id="wrapper">
        <!-- sidebar -->
        <div class="sidebar" :class="{ showOverlay: overlayVisibility }">
            <span class="closeButton" @click="hideOverlay">&times;</span>
            <p class="brand-title"><a href="">Alphayo Blog</a></p>

            <div class="side-links">
                <ul>
                    <li>
                        <router-link @click="hideOverlay" :to="{ name: 'Home' }">Home</router-link>
                    </li>
                    <li>
                        <router-link @click="hideOverlay" :to="{ name: 'Blog' }">Blog</router-link>
                    </li>
                    <li>
                        <router-link @click="hideOverlay" :to="{ name: 'About' }">About</router-link>
                    </li>
                    <li>
                        <router-link @click="hideOverlay" :to="{ name: 'Contact' }">Contact</router-link>
                    </li>
                </ul>
            </div>

            <!-- sidebar footer -->
            <footer class="sidebar-footer">
                <div>
                    <a href=""><i class="fab fa-facebook-f"></i></a>
                    <a href=""><i class="fab fa-instagram"></i></a>
                    <a href=""><i class="fab fa-twitter"></i></a>
                </div>

                <small>2022 Komar Natalia Blog.</small>
            </footer>
        </div>
        <!-- Menu Button -->
        <div class="menuButton" @click="ShowOverlay">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
        </div>
        <!-- main -->
        <main class="container">
            <!-- render components on the page visited-->
        </main>
        <router-view></router-view>
        <!-- Main footer -->
        <footer class="main-footer">
            <div>
                <a href=""><i class="fab fa-facebook-f"></i></a>
                <a href=""><i class="fab fa-instagram"></i></a>
                <a href=""><i class="fab fa-twitter"></i></a>
            </div>
            <small>2022 Komar Natalia Blog</small>
        </footer>
    </div>
</template>
<script>
export default {
    data() {
        return {
            overlayVisibility: false,
        };
    },
    methods: {
        ShowOverlay() {
            this.overlayVisibility = true;
        },
        hideOverlay() {
            this.overlayVisibility = false;
        },
    },
};
</script>
<style scoped>
.showOverlay {
    width: 100%;
    z-index: 5;
}
</style>
