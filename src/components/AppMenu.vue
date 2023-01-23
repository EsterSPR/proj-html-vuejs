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

<style lang="">
    
</style>