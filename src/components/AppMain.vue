<script>

import AppMainCategories from './AppMainCategories.vue';

export default {
    data(){
        return{
            foodCorner:[
                {
                    img: '../../public/img/single-post-img3-1200x790.jpg',
                    recipe: 'Food Corner: Top Japanese Restaurants for Sushi',
                    jumbotron: true,

                },
                {
                    img: '../../public/img/fi-roundup-1200x790.jpg',
                    recipe: 'Roundup: My New Favourite Recipes For Healthy Living',
                    jumbotron: false,

                },
                {
                    img: '../../public/img/fi-toasts-1200x790.jpg',
                    recipe: 'Why These Toasts with Tea are My New Favorite',
                    jumbotron: false,

                }
            ],
            popularRecipes:[
                {
                    img: '../../public/img/Yogurt-Nan-1200x790.jpg',
                    recipe: 'Lunch Favourite with Salad, Naan And Beans',
                    main: true,
                    bottom: true,
                },
                {
                    img: '../../public/img/Mixed-fruits-1200x790.jpg',
                    recipe: 'Fruit Platter with Banana, Mango, Berries and Orange',
                    main: false,
                    bottom: true,
                },
                {
                    img: '../../public/img/r-rachel-park-366508-unsplash-min-1200x790.jpg',
                    recipe: 'Breakfast Delight With Strawberry, Egg And Fruits',
                    main: false,
                    bottom: true,
                },
                {
                    img: '../../public/img/r-michelle-tsang-500721-unsplash-min-1200x790.jpg',
                    recipe: 'Ice Cream Heaven With Vanilla, Chocolate And Pistachio',
                    main: false,
                    bottom: true,
                },
                {
                    img: '../../public/img/quick-summer-drink-460x295.jpg',
                    recipe: 'Video Recipe: How to Make a Cool Summer Drink',
                    main: false,
                    bottom: false,
                },
                {
                    img: '../../public/img/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg',
                    recipe: 'Ketogenic Diet Recipe with Avocado',
                    main: false,
                    bottom: false,
                },
                {
                    img: '../../public/img/perfect-cosmopolitan-460x295.jpg',
                    recipe: 'Video Recipe: The Perfect Cosmopolitan',
                    main: false,
                    bottom: false,
                },
                {
                    img: '../../public/img/fi2x-6-460x295.jpg',
                    recipe: 'Summer Cheese Platter with Berries, Crackers and Wine',
                    main: false,
                    bottom: false,
                },
                {
                    img: '../../public/img/r-brooke-lark-96398-unsplash-min-460x295.jpg',
                    recipe: 'Strawberry Fruit Pies Served With Tea',
                    main: false,
                    bottom: false,
                },
            ]
        }
    },
    components:{
        AppMainCategories,
    }
}
</script>

<template lang="">
    <div class="jumbotron">
        <div class="card jumbotron-title-container">
            <div class="jumbotron-title-badge"><h6> TODAY'S PICK </h6></div>
            <div class="jumbotron-title" v-for="rec, index in foodCorner" :class="(rec.jumbotron === false) ? ' d-none' : ''"> <a href="#"><h1 class="recipe-title">{{ rec.recipe }}</h1></a> </div>
            <div class="recipe-date">March 25, 2019</div>
        </div>
    </div>

    <div class="foodie-journal-container">
        <div class="row">
            <div class="col-5"><hr></div>
            <div class="col-2 mb-3"><h5>FOODIE JOURNAL</h5></div>
            <div class="col-5"><hr></div>
        </div>
        <div class="row">
            <div class="col-4" v-for="rec, index in foodCorner">
                <div class="foodie-card">
                <img :src="rec.img" class="foodie-card-image">
                <div class="foodie-card-overlay">
                    <div class="foodie-overlay-text recipe-title">
                        <fa icon="link" class="recipe-ico" />
                        <h5>{{rec.recipe}}</h5>
                    </div>
                </div>
                </div>
                <div class="foodie-card-undetext text-center mt-2">
                    <h4 class="recipe-title"><a href="#">{{rec.recipe}}</a></h4>
                    <p>By <a href="#">admin</a> | <span class="recipe-date">March 25, 2019</span></p>
                </div>
            </div>
        </div>
    </div>

    <div class="popular-recipes-container">
        <div class="row mb-5">
            <div class="col-4"></div>
            <div class="col-4 text-center">
                <h5>POPULAR RECIPES</h5>
                <p>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
            </div>
            <div class="col-4"></div>
        </div>

        <div class="row">

            <div class="col-6">
                <div v-for="rec, index in popularRecipes" class="foodie-card" :class="(rec.main === false) ? ' d-none' : ''">
                    <img :src="rec.img" class="foodie-card-image">
                    <div class="foodie-card-overlay">
                        <div class="foodie-overlay-text recipe-title">
                            <fa icon="link" class="recipe-ico" />
                            <h5>{{rec.recipe}}</h5>
                        </div>
                    </div>
                </div>

                <div class="popular-recipes-main" v-for="rec, index in popularRecipes" :class="(rec.main === false) ? ' d-none' : ''">
                    <div class="row">
                        <div class="col-12">
                            <h4 class="recipe-title"><a href="#">{{rec.recipe}}</a></h4>
                            <a href="#">Bakery</a>, <a href="#">Featured</a>, <a href="#">Healthy</a>, <a href="#">Latest Recipes</a>, <a href="#">Staff Picks</a>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-12"><hr></div>
                    </div>
                    <div class="row">
                        <div class="col-12">
                            <p>Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex. Sed porttitor, diam eget convallis volutpat, arcu tellus facilisis nulla, id dignissim orci leo id.</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-12">
                            <button class="main-button">LEARN MORE</button>
                        </div>
                    </div>
                </div>

            </div>

            <div class="col-6 d-flex flex-wrap">
                <div v-for="rec, index in popularRecipes" class="foodie-card popular-recipes-card" :class="(rec.main === true) ? ' d-none' : ''">
                    <img :src="rec.img" class="foodie-card-image">
                    <div class="foodie-card-overlay">
                        <div class="foodie-overlay-text recipe-title">
                            <fa icon="link" class="recipe-ico" />
                            <h5>{{rec.recipe}}</h5>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <AppMainCategories />

    <div class="subscribe">
        <div class="subscribe-text-container">
            <h2 class="recipe-title mb-3">Subscribe <span>&</span> Receive A Free eBook</h2>
            <p>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
            <form class="row my-5">
                <div class="col-8">
                    <input type="email" class="form-control main-input" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Insert your email ... *" required>
                </div>
                <div class="col-4">
                    <button type="submit" class="main-button input-button">SUBSCRIBE</button>
                </div>
            </form>
            <p class="subscribe-text-small">Cras porttitor pellentesque sem eu pretium.</p>
        </div>
    </div>

    <div class="d-flex w-100">
        <div v-for="rec, index in popularRecipes" class="foodie-card popular-recipes-card" :class="(rec.bottom === false) ? ' d-none' : ''">
            <img :src="rec.img" class="foodie-card-image">
            <div class="foodie-card-overlay">
                <div class="foodie-overlay-text recipe-title">
                    <fa icon="link" class="recipe-ico" />
                    <h5>{{rec.recipe}}</h5>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
    .jumbotron{
        width: 100vw;
        background-image: url(../../public/img/slide1-bg.jpeg);
        background-size: cover;
        text-align: center;
        padding: 200px 200px 300px 200px;

        .jumbotron-title-container{
            background-color: $food-white;
            width: 700px;
            padding: 50px;
            margin: 0 auto;
            position: relative;
            border: none !important;

            .jumbotron-title-badge{
                background-color: $food-orange;
                width: fit-content;
                margin: 0 auto;
                padding: 10px 20px 5px 20px;
                border-radius: 10px;
                position: absolute;
                top: -20px;
                left: 39%;
                color: $food-white;
            }
        }
    }

    .foodie-card {
            position: relative;
            transition: all .5s ease-in;
        }

        .foodie-card-image {
            display: block;
            width: 100%;
            height: auto;
        }

        .foodie-card-overlay {
            position: absolute;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
            height: 100%;
            width: 100%;
            opacity: 0;
            visibility: none;
            transition: .5s ease;
            background-image: linear-gradient(rgba(252, 117, 35, 0.7), rgba(252, 117, 35, 1));
        }

        .foodie-card:hover .foodie-card-overlay {
            opacity: 1;
            cursor: pointer;
        }

        .foodie-overlay-text {
            color: white;
            font-size: 20px;
            position: absolute;
            top: 50%;
            left: 50%;
            -webkit-transform: translate(-50%, -50%);
            -ms-transform: translate(-50%, -50%);
            transform: translate(-50%, -50%);
            text-align: center;
        }

    .foodie-journal-container{
        width: calc(100% - 200px);
        height: auto;
        padding: 30px;
        margin: -100px 100px 100px 100px;
        background-color: $food-white;
    }

    .popular-recipes-container{
        padding: 0 100px;

        p{
            color: $food-darkgray;
        }

        .popular-recipes-card{
            margin: 0 5px 15px 5px;
            width: calc(50% - 10px)
        }

        .popular-recipes-main{
            background-color: $food-white;
            padding: 50px;

            p{
                font-size: 13pt;
                line-height: 35px;
                text-align: justify;
            }
        }
    }

    .main-button{
        padding: 10px 30px;
        background-color: $food-orange;
        border: none;
        color: $food-white;
        font-weight: bolder;
        transition: 0.3s;
    }

    .main-button:hover{
        background-color: $food-darkorange;
    }

    .subscribe{
        width: 100vw;
        background-color: $food-white;
        background-image: url(../../public/img/subscribe-sec-bg.png);
        background-size: cover;
        background-position: center;
        text-align: center;
        padding: 100px 200px 100px 200px;

        .subscribe-text-container{
            width: 700px;
            padding: 50px;
            margin: 0 auto;

            span{
                color: $food-orange;
            }

            p{
                color: $food-darkgray;
                font-size: 13pt;
            }

            .input-button{
                height: 50px;
                width: 100%;
            }

            .main-input{
                height: 50px
            }

            .main-input:hover{
                border-color: $food-orange;
            }

            .subscribe-text-small{
                font-size: 10pt;
            }
        }
    }
</style>