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

    .menu{
        margin: 0 0 25px 0;
    }
    .menuvoice{
        padding: 0px 150px 0px 0px;
        font-weight: 100;
    }

    .menuvoice:hover{
        color: $food-orange;
        border-right: 2px solid $food-orange;
    }
</style>