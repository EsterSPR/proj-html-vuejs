<script>
export default {
    data(){
        return{
            mainIcons: [
                {
                    icon: '../../public/img/drinks-recipes.png',
                    title: 'DRINKS'
                },
                {
                    icon: '../../public/img/soups-recipes.png',
                    title: 'SOUPS'
                },
                {
                    icon: '../../public/img/baking-recipes.png',
                    title: 'BAKERY'
                },
                {
                    icon: '../../public/img/dinner-recipes.png',
                    title: 'DINNER'
                },
                {
                    icon: '../../public/img/healthy-recipes.png',
                    title: 'HEALTHY'
                },
                {
                    icon: '../../public/img/staff-picks.png',
                    title: 'STAFF PICKS'
                },
                {
                    icon: '../../public/img/premium-recipes.png',
                    title: 'APPETISERS'
                },
                {
                    icon: '../../public/img/quick-easy-recipes.png',
                    title: 'QUICK & EASY'
                }
            ],
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
                },
                {
                    img: '../../public/img/Mixed-fruits-1200x790.jpg',
                    recipe: 'Fruit Platter with Banana, Mango, Berries and Orange',
                },
                {
                    img: '../../public/img/r-rachel-park-366508-unsplash-min-1200x790.jpg',
                    recipe: 'Breakfast Delight With Strawberry, Egg And Fruits',
                },
                {
                    img: '../../public/img/r-michelle-tsang-500721-unsplash-min-1200x790.jpg',
                    recipe: 'Ice Cream Heaven With Vanilla, Chocolate And Pistachio',
                },
                {
                    img: '../../public/img/quick-summer-drink-460x295.jpg',
                    recipe: 'Video Recipe: How to Make a Cool Summer Drink',
                },
            ]
        }
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
                    <h4 class="recipe-title">{{rec.recipe}}</h4>
                    <p>By <a href="#">admin</a> | <span class="recipe-date">March 25, 2019</span></p>
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

    .foodie-journal-container{
        width: calc(100% - 200px);
        height: auto;
        padding: 30px;
        margin: -100px 100px 100px 100px;
        background-color: $food-white;

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
    }
</style>