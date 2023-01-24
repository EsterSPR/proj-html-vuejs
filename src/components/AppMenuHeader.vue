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
        padding: 0px 10px 10px 10px;
        font-weight: bold;
    }

    .menuactive{
        color: $food-orange;
        border-bottom: 2px solid $food-orange;
    }
</style>