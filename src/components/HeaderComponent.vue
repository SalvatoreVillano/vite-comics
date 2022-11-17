<template>
    <header>
        <div class="container justify-content-between">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="DC Comics logo">
            </a>
            <nav>
                <ul>
                    <li v-for="(item, index) in navBar" :key="index">
                        <a :href="item.url" :class="{ 'active': item.current }">{{ item.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            navBar: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: false,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

header {

    div {
        height: 150px;
        @include dflex;

        nav ul {
            @include dflex;

            li a {
                color: black;
                padding: .8rem;
                font-size: .8rem;
                text-transform: uppercase;
                font-weight: 700;

                &.active,
                &:hover {
                    color: #0C7CEC;
                }
            }
        }
    }
}
</style>