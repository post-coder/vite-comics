<script>
export default {
    name: 'AppFooter',

    data() {
        return {
            linkList: [
                    {
                        title: 'dc comics',
                        links:['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                    },
                    {
                        title: 'shop',
                        links:['Shop DC', 'Shop DC Collectibles']
                    },
                    {
                        title: 'dc',
                        links:['Terms of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                    },
                    {
                        title: 'sites',
                        links:['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                    },
            ],

            socials: [
                {
                    name: 'facebook',
                    icon: '/img/footer-facebook.png'
                },
                {
                    name: 'twitter',
                    icon: '/img/footer-twitter.png'
                },
                {
                    name: 'youtube',
                    icon: '/img/footer-youtube.png'
                },
                {
                    name: 'pinterest',
                    icon: '/img/footer-pinterest.png'
                },
                {
                    name: 'periscope',
                    icon: '/img/footer-periscope.png'
                },
            ]
        }
    }
}
</script>

<template>

    <footer>
        <div class="footer-top">
            <div class="container">

                <div class="links">
    
                    <div v-for="currentLinkList in linkList" class="link-list">
                        <h4>{{ currentLinkList.title }}</h4>
                        <ul>
                            <li v-for="currentLink in currentLinkList.links">{{ currentLink }}</li>
                            
                        </ul>
                    </div>
                    
                </div>
    
                <div class="big-logo">
                    <img src="/img/dc-logo-bg.png" alt="">
                </div>

            </div>
        </div>

        <div class="footer-bottom">
            <div class="container">

                <div class="cta">
                    <button class="btn">
                        Sign-up now!
                    </button>
                </div>

                <div class="social-links">
                    <strong>Follow Us</strong>
                    <ul>
                        <li v-for="currentSocial in socials">
                            <img :src="currentSocial.icon" :alt="currentSocial.name">
                        </li>
                        
                    </ul>
                </div>

            </div>
        </div>
    </footer>

</template>

<style lang="scss">
@use '../styles/general' as *;
@use '../styles/variables' as *;


footer {

    ul {
        list-style: none;
        padding: 0;
    }

    .footer-top {
        height: 370px;

        background-image: url('/img/footer-bg.jpg');
        background-position: cover;

        overflow: hidden;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            height: 100%;
        }


        .links {
            display: flex;
            flex-flow: column wrap;
            align-content: flex-start;
            gap: 20px 30px;

            height: 100%;

            padding: 20px 0;

            h4 {
                text-transform: uppercase;
                font-size: 1.5em;
                font-family: 'Barlow Condensed', sans-serif;

                margin-bottom: 10px;
            }

            ul {
                color: #ccc;
                font-size: .9em;
            }
        }
    }

    .footer-bottom {
        padding: 20px 0;
        background-color: #303030;

        .btn {
            padding: 14px 18px;
            text-transform: uppercase;
            font-weight: bold;
            font-size: 1em;

            background-color: transparent;
            border: solid 1px $primary;
        }

        .container {
            display: flex;
            justify-content: space-between;
            
            .social-links, ul {
                display: flex;
                align-items: center;
                gap: 18px;

                strong {
                    color: $primary;
                    text-transform: uppercase;
                    font-family: 'Barlow Condensed', sans-serif;
                    font-size: 1.3em;
                }
            }
        }
    }

    
}
</style>