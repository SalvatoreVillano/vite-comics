<template>
    <main>
        <div class="container-fluid">
            <span>Current Series</span>
            <div class="cardList">
                <div class="cards" v-for="(item, index) in cardList" :key="index">
                    <div class="mycard">
                        <img :src="item.thumb" :alt="item.series">
                    </div>
                    <p class="text-white text">{{ item.series }}</p>

                </div>
            </div>
        </div>
    </main>
</template>

<script>
import { listComics } from '../assets/dc-comics';
export default {
    name: 'MainComponent',
    data() {
        return {
            cardList: listComics,
        }
    }
}

</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;




.mycard {
    max-width: 150px;
    max-height: 150px;
    overflow: hidden;

}

.container-fluid {
    background-color: rgb(28, 28, 28);
    height: 300px;

    .cardList {
        @include dflex;
        gap: 5px
    }

    .cards {
        width: calc((100% / 6));
    }


}
</style>