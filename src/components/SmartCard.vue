<script>
export default {
    name: 'SmartCard',

    props: {
        imagePath: String,
        titleURL: String,
        titleText: String,
        paragraphText: String
    }
}
</script>

<template>
    <div class="smart-card">
        <div class="thumbnail">
            <img :src="imagePath" :alt="titleText">
        </div>

        <h4>
            <a :href="titleURL">
                {{ titleText }}
            </a>
        </h4>

        <p>
            {{ paragraphText }}
        </p>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.smart-card {
    width: 100%;
    height: 100%;
    border-radius: $rad-xl;
    padding: 2.25rem 1rem;
    border: 1px solid #b2b5d2;
    background-color: #fff1e8;
    background-image: linear-gradient(180deg, $white, #fff1e8);
    box-shadow: 0 .5rem 1.125rem 0 #eaeaee;
    transition: all $trns-stnd;

    &:hover {
        border-color: $white;
        background-image: linear-gradient(0deg, $white, #fff1e8);
    }

    .thumbnail {
        height: 5rem;
        margin-bottom: 2rem;

        img {
            height: 100%;
        }
    }

    h4 {
        margin-bottom: .625rem;
    }
}
</style>