<script>
export default {
    name: 'BlueLinks',

    data() {
        return {

            links: [

                {
                    title: 'Digital Comics',
                    image: 'buy-comics-digital-comics.png'
                },

                {
                    title: 'DC Merchandise',
                    image: 'buy-comics-merchandise.png'
                },

                
                {
                    title: 'Subscription',
                    image: 'buy-comics-subscriptions.png'
                },

                {
                    title: 'Comic shop locator',
                    image: 'buy-comics-shop-locator.png'
                },

                {
                    title: 'DC Power Visa',
                    image: 'buy-dc-power-visa.svg'
                },

            ],

        }
    }
}

</script>

<template>

    <div id="blue-links">
        <div class="container">
            <div class="row">

                <div v-for="link in links" class="col">
                    <img :src="'/img/' + link.image" alt="Buy digital comics">
                    <span>{{ link.title }}</span>
                </div>

            </div>
        </div>
    </div>

</template>

<style lang="scss">
@use '../styles/variables' as *;


#blue-links {
    background-color: $primary;

    .row {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 70px;

        padding: 50px;

        .col {
            display: flex;
            align-items: center;
            gap: 20px;

            height: 55px;

            img {
                max-width: 55px;
                height: 100%;
            }
        }
    }
}
</style>