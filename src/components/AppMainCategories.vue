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
            ]
        }
    }
}
</script>

<template lang="">

    <div class="culinary-collection-container">

        <div class="row mb-5">
                <div class="col-4"></div>
                <div class="col-4 text-center">
                    <h5>CULINARY COLLECTION</h5>
                    <p>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
                </div>
                <div class="col-4">
                </div>
            </div>

            <div class="row">
                <div class="col-12 d-flex flex-wrap justify-content-between">
                    <div class="culinary-collection text-center" v-for="icon, index in mainIcons">
                        <div class="row">
                            <div class="col-12"><img :src="icon.icon" :alt="icon.title"></div>
                            <div class="col-12"> <button class="culinary-collection-button w-100">{{ icon.title }}</button> </div>
                        </div>
                    </div>
                </div>
            </div>

        </div>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.culinary-collection-container{
    padding: 0 100px;
    margin-top: 100px;

        p{
            color: $food-darkgray;
        }

        .culinary-collection{
            background-color: $food-white;
            width: 250px;
            margin-bottom: 50px;

            img{
                margin: 10px;
                width: 100px;
                transition: 0.3s;
            }

            img:hover{
                transform: scale(1.2);
            }

            button{
                background-color: $food-white;
                border: none;
                padding: 15px;
                font-weight: bolder;
                transition: 0.3s;
            }

            button:hover{
                background-color: $food-orange;
                color: $food-white;
            }
        }
}
    
</style>