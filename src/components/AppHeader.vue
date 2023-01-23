<script>

import AppSocial from './AppSocial.vue';

export default {
    props:{
        voices: String,
        urls: URL,
        actives: Boolean,
    },
  data(){
    return{
        menuHeader: [
                {
                    voice: 'Home',
                    url: '#',
                    active: true,
                },
                {
                    voice: 'Recipes',
                    url: '#',
                    active: false,
                },
                {
                    voice: 'Places',
                    url: '#',
                    active: false,
                },
                {
                    voice: 'Blog',
                    url: '#',
                    active: false,
                },
                {
                    voice: 'About',
                    url: '#',
                    active: false,
                },
                {
                    voice: 'Contact',
                    url: '#',
                    active: false,
                },
                {
                    voice: '<fa icon="magnifying-glass" />',
                    url: '#',
                    active: false,
                }
            ],
            socialIcons: [
                {
                    name: 'Facebook',
                    ico: 'facebook',
                    link: '#',
                },
                {
                    name: 'Instagram',
                    ico: 'instagram',
                    link: '#',
                },
                {
                    name: 'Twitter',
                    ico: 'twitter',
                    link: '#',
                },
                {
                    name: 'YouTube',
                    ico: 'youtube',
                    link: '#',
                },
                {
                    name: 'TikTok',
                    ico: 'tiktok',
                    link: '#',
                },
                {
                    name: 'Pinterest',
                    ico: 'pinterest',
                    link: '#',
                }
            ]
        }
  },
  components:{
        AppSocial,
    },
}
</script>

<template>
<header class="container">
    
  <div class="row">
    <div class="col-3"> <a href="#" class="mx-2">Download App <span class="badge">iOS</span></a> <a href="#">Advertise with us</a> </div>
    <div class="col-6 text-center"><img src="img/avada-food-logo-2x.png" alt="logo" class="logo-header"></div>
    <div class="col-3 d-flex text-right">
        <div v-for="icon, index in socialIcons" :key="index" class="header-ico-container">
            <span tabindex="0" data-bs-toggle="popover" data-bs-trigger="hover focus" data-bs-placement="bottom" :data-bs-content="icon.name"> <a :href="icon.link"><fa :icon="['fab', icon.ico]" class="icon" /> </a> </span>
        </div>
    </div>
  </div>

  <div class="row">
    <div class="col-12 d-flex">
        <div v-for="item, index in menuHeader" :key="index" 
        :voices="item.voice" 
        :urls="item.url" 
        :actives="item.active">
            <a :href="urls">
                {{ voices }}
            </a>
        </div>
    </div>
  </div>

</header>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

    header{
        width: 100vw;
        padding: 30px;
        background-color: $food-lightgray;

        .badge{
                background-color: $food-orange;
            }

        img[alt="logo"]{
            height: 120px;
        }

        .icon {
            color: $food-darkgray;
            background-color: rgba(255, 255, 255, 0);
            transition: background-color 0.3s;
            height: 17px;
            padding: 10px;
            border-radius: 5px;
        }

        .icon:hover {
            background-color: rgba(255, 255, 255, 1)
        }

    }
</style>