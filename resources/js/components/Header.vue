<template>
    <div class="container">
        <header class="d-flex justify-content-lg-center py-3">
            <nav class="navbar navbar-expand-lg">
                <button
                    class="navbar-toggler"
                    type="button"
                    data-mdb-toggle="collapse"
                    data-mdb-target="#navbarToggleExternalContent"
                    aria-controls="navbarToggleExternalContent"
                    aria-expanded="false"
                    aria-label="Toggle navigation"
                >
                    <i class="fas fa-bars"></i>
                </button>
                <ul class="nav nav-pills collapse navbar-collapse">
                    <!-- faccio v-for per girare sull'array e fare le voci del menu -->
                    <li
                        class="nav-item"
                        v-for="item in menuItems"
                        :key="item.id"
                    >
                        <!-- comando router-link mi permette di linkare la voce alla rotta nel front.js -->
                        <!-- se il link è attivo attribuiamo la classe active come scritto nel front.js -->
                        <router-link
                            class="nav-link"
                            exact-active-class="active"
                            :to="{ name: item.routeName }"
                            >{{ item.label }}</router-link
                        >
                    </li>
                </ul>
            </nav>
        </header>
        <div class="collapse" id="navbarToggleExternalContent">
            <div
                class="d-flex flex-column align-items-center bg-light shadow-3 p-4"
            >
                <button
                    v-for="item in menuItems"
                    :key="item.id"
                    class="btn w-25 m-1"
                >
                    <router-link
                        class="nav-link"
                        exact-active-class="active"
                        :to="{ name: item.routeName }"
                        >{{ item.label }}</router-link
                    >
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            // creo array con voci per il v-for nella navbar
            menuItems: [
                {
                    label: "Home",
                    routeName: "home",
                },
                {
                    label: "Portfolio",
                    routeName: "portfolio",
                },
                {
                    label: "About",
                    routeName: "about",
                },
            ],
        };
    },
};
</script>

<style lang="scss"></style>
