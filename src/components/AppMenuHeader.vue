<script>
export default {
    props: {
        voices: String,
        urls: URL,
        actives: Boolean,
    },
}
</script>

<template lang="">
    <div class="mx-2 menu">
        <a :href="urls" class="menuvoice" :class="(actives === true) ? ' menuactive' : ''">
            {{ voices }}
        </a>
    </div>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
    .menuvoice{
        margin: 0 20px;
        font-weight: bold;
        display: inline-block;
    }

    .menuvoice::after {
        content: '';
        display: block;
        width: 0;
        height: 2px;
        background: $food-orange;
        transition: width .3s;
    }

    .menuvoice:hover::after {
        width: 100%;
    }

    .menuactive{
        color: $food-orange;
        border-bottom: 2px solid $food-orange;
    }

    .menuactive::after{
        height: 0px;
    }
</style>