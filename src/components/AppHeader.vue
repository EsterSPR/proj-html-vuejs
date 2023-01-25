<script>

import AppMenuHeader from './AppMenuHeader.vue';

export default {
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
                }
            ],
            socialIcons: [
                {
                    name: 'Facebook',
                    ico: 'facebook-f',
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
                    ico: 'pinterest-p',
                    link: '#',
                }
            ]
        }
  },
  components:{
    AppMenuHeader
  }
}
</script>

<template>
<header>
    
  <div class="row mb-4">
    <div class="col-3 topleft-header"> <a href="#" class="mx-2">Download App <span class="badge">iOS</span></a> <a href="#">Advertise with us</a> </div>
    <div class="col-6 text-center"><img src="img/avada-food-logo-2x.png" alt="logo" class="logo-header"></div>
    <div class="col-3 d-flex text-right">
        <div v-for="icon, index in socialIcons" :key="index" class="header-ico-container">
            <a :href="icon.link"><fa :icon="['fab', icon.ico]" class="icon" /> </a>
        </div>
    </div>
  </div>

  <div class="row">
    <div class="col-12 d-flex justify-content-center">
        <AppMenuHeader v-for="item, index in menuHeader" :key="index" 
        :voices="item.voice" 
        :urls="item.url" 
        :actives="item.active" />
        <a href="#" class="menuvoice"><fa icon="magnifying-glass" /></a>
    </div>
  </div>

</header>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

    header{
        width: 100vw;
        padding: 30px 100px;
        background-color: $food-lightgray;
        font-family: 'Catamaran', sans-serif !important;

        .topleft-header{
            font-size: 11pt;

            .badge{
                background-color: $food-orange;
            }
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

        .menuvoice{
            margin: 0 20px;
        }

    }
</style>