<template>
    <div class="container-fluid justify-content-between">
        <a href=#>Sign-Up Now!</a>
        <div>
            <h3>Follow us</h3>
            <ul>
                <li v-for="(item, index) in list">
                    <img :src="item.url" class="gap-2">
                </li>
            </ul>
        </div>
    </div>
</template>
            
<script>
export default {
    name: 'SubFooterComponent',
    data() {
        return {
            list: [
                {
                    name: 'Facebook',
                    url: '/img/footer-facebook.png',
                },
                {
                    name: 'Twitter',
                    url: '/img/footer-twitter.png',
                },
                {
                    name: 'YouTube',
                    url: '/img/footer-youtube.png',
                },
                {
                    name: 'Pinterest',
                    url: '/img/footer-pinterest.png',
                },
                {
                    name: 'Periscope',
                    url: '/img/footer-periscope.png',
                }
            ]
        }
    }
}
</script>
            
<style lang ="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

.container-fluid {
    @include dflex;
    background-color: rgb(48, 48, 48);
    height: 100px;
    padding: 25px;
    padding-left: 15%;
    padding-right: 15%;



    a {
        text-transform: uppercase;
        color: white;
        border: 3px solid #0C7CEC;
        padding: 1rem;
    }

    div {
        @include dflex;

        h3 {
            color: #0C7CEC;
            font-weight: 700;
        }

        ul {
            @include dflex;
            gap: 20px;

            li {
                cursor: pointer;
            }
        }
    }


}
</style>