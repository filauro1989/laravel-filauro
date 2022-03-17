<template>
    <div class="container">
        <header class="d-flex justify-content-center py-3">
            <ul class="nav nav-pills">
                <!-- faccio v-for per girare sull'array e fare le voci del menu -->
                <li class="nav-item" v-for="item in menuItems" :key="item.id">
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
        </header>
    </div>
</template>

<script>
export default {
    name: "Header",
};
</script>

<style lang="scss"></style>
