<script>
export default {
    props: {
        titles: String,
        links: URL,
        icons: Image,
    }
}
</script>

<template>

    <div class="wrapper d-flex">
        <div class="mx-2 menu">
            <span class="d-inline-block" tabindex="0" data-bs-toggle="popover" data-bs-placement="bottom" data-bs-trigger="hover focus" :data-bs-content="titles"> <a :href="links" class="icon"><img :src="icons" :alt="titles"></a> </span>
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .menu{
        cursor: pointer;

        .icon {
            fill: black; 
        }

        .icon:hover {
            fill: orange;
        }
    }
</style>