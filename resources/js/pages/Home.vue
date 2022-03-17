<template>
    <div class="home-container container vh-100">
        <div class="row mt-5">
            <div class="col-md-6 col-12 p-3">
                <div class="img-wrapper w-100">
                    <img class="w-100" :src="profilePic" alt="ProfilePic" />
                </div>
            </div>
            <div
                class="col-md-6 col-12 p-3 d-flex justify-content-center align-items-center"
            >
                <div class="description-wrapper text-center">
                    <h1>JR Full Stack Web Developer</h1>
                    <p>
                        Junior Full Stack Web Developer in formazione presso
                        Boolean Careers. <br />
                        Mi ritengo una persona estremamente versatile.<br />
                        Team Working ed evoluzione come costanti nella mia vita.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Home",
    data() {
        return {
            profilePic: require("../../image/PrimoPiano.jpg"),
        };
    },
};
</script>

<style lang="scss"></style>
