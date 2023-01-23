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
        padding: 0px 5px 30px 5px;
    }

    .menuactive{
        color: $food-orange;
        border-bottom: 3px solid $food-orange;
    }
</style>