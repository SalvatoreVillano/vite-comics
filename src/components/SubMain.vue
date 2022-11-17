<template>
    <div class="container-fluid justify-content-around pt-4">
        <ul>
            <li v-for="(item, index) in list" :key="index">
                <div class="list-item">
                    <img :src="item.img" alt="item.text">
                    <p class="ms-4">
                        {{ item.text }}
                    </p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'SubMain',
    data() {
        return {
            list: [
                {
                    text: "Digital Comics",
                    url: "#",
                    img: "/img/buy-comics-digital-comics.png",
                },
                {
                    text: "DC Merchandise",
                    url: "#",
                    img: "/img/buy-comics-merchandise.png",
                },
                {
                    text: "Subscription",
                    url: "#",
                    img: "/img/buy-comics-subscriptions.png",
                },
                {
                    text: "Comic Shop Locator",
                    url: "#",
                    img: "/img/buy-comics-shop-locator.png",
                },
                {
                    text: "DC Power Visa",
                    url: "#",
                    img: "/img/buy-dc-power-visa.svg",
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

.container-fluid {
    @include dflex;
    background-color: rgb(2, 130, 249);
    height: 150px;

    ul {
        @include dflex;

        li .list-item {
            @include dflex;
            padding: 2rem;
            font-size: .7rem;

            p {
                text-transform: uppercase;
                color: white
            }

            img {
                width: 50px;

            }
        }
    }
}
</style>