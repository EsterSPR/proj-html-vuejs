<script>

import AppMenuFooter from './AppMenuFooter.vue';

export default {
  data(){
    return{
      menuFooter: [
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
                    voice: 'Blog ',
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
            ]
    }
  },
  components:{
    AppMenuFooter,
  }
}
</script>

<template>
  <footer>
    <div class="row footer-top">
      <div class="col-3">
        <div class="row">
          <div class="col align-items-center">
            <img src="../../public/img/avada-food-logo-mob-2x.png" alt="logo">
            </div>
        </div>
        <div class="row">
          <div class="col-12 d-flex align-items-center">
            <div v-for="icon, index in socialIcons" :key="index" class="header-ico-container">
                <span tabindex="0" data-bs-toggle="popover" data-bs-trigger="hover focus" data-bs-placement="bottom" :data-bs-content="icon.name"> <a :href="icon.link"><fa :icon="['fab', icon.ico]" class="icon" /> </a> </span>
            </div>
          </div>
        </div>
      </div>
      <div class="col-3">
        <AppMenuFooter v-for="item, index in menuFooter" :key="index" 
        :voices="item.voice" 
        :urls="item.url" 
        :actives="item.active" />
      </div>
      <div class="col-3">

        <div class="row">
          <div class="col-12"><h6>CONTACT US</h6></div>
        </div>

        <div class="row contacts-footer">
          <div class="col-2">
            <fa icon="location-dot" class="footer-ico" />
          </div>
          <div class="col-10">
            775 New York Ave, Brooklyn,<br> Kings, New York 11203
          </div>
        </div>
        <div class="row">
          <div class="col-11"><hr></div>
          <div class="col-1"></div>
        </div>

        <div class="row contacts-footer">
          <div class="col-2">
            <fa icon="phone-flip" class="footer-ico" />
          </div>
          <div class="col-10">
            + 0100-505-0000
          </div>
        </div>
        <div class="row">
          <div class="col-11"><hr></div>
          <div class="col-1"></div>
        </div>

        <div class="row contacts-footer">
          <div class="col-2">
            <fa icon="envelope" class="footer-ico" />
          </div>
          <div class="col-10">
            info@your-domain.com
          </div>
        </div>
        <div class="row">
          <div class="col-11"><hr></div>
          <div class="col-1"></div>
        </div>

      </div>
      <div class="col-3">
        <div class="row">
          <div class="col-12"><h6>GET OUR APP</h6></div>
        </div>

        <div class="row">
          <div class="col-12"><a href="#"><img src="../../public/img/download-android.png" alt="download"></a></div>
        </div>

        <div class="row">
          <div class="col-12"><a href="#"><img src="../../public/img/download-app-store.png" alt="download"></a></div>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      © Copyright 2012 - 2019 • Avada Food by <a href="#">Theme Fusion</a> • All Rights Reserved • Powered by <a href="#">WordPress</a>
    </div>
  </footer>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

footer{
  width: 100vw;
  background-color: $food-white;
  font-family: 'Catamaran', sans-serif;

  .footer-top{
    padding: 70px 100px;
    margin-right: 0 !important;

    img[alt="logo"]{
    width: 200px;
    margin-bottom: 20px;
  }

  .icon {
    color: $food-darkgray;
    background-color: rgba(255, 255, 255, 0);
    transition: background-color 0.3s;
    height: 20px;
    padding: 10px;
    border-radius: 5px;
    transition: 0.3s;
  }

  .icon:hover {
    color: lighten($color: $food-darkgray, $amount: 15);
  }

  .contacts-footer{
    margin: 5px 0 5px -10px;
    padding-right: 20px;
    color: $food-darkgray;

    .footer-ico{
      color: $food-orange;
    }
  }

  h6{
      color: $food-orange;
      font-weight: bold;
      margin-bottom: 20px;
    }

  img[alt="download"]{
      width: 200px;
      margin: 5px 0;
    }
  }

    .footer-bottom{
      background-color: $food-lightgray;
      padding: 30px;
      text-align: center;
      width: 100%;
      color: $food-darkgray;
    }
}
  
</style>