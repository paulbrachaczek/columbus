<template>
    <div v-if=images class="m-slider">
        <figure class="m-slider__main a-figure">
            <img itemprop="image" :src="`/img/${mainpic}`" alt="">
        </figure>
        <ul class="m-slider__list">
            <li class="m-slider__element" v-for="image in images" :key={image}>
                <figure class="a-figure" @click.prevent="changeImg(image)">
                    <img itemprop="image" :src="`/img/${image}`" :alt=image>
                </figure>
            </li>
        </ul>    
    </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Slider extends Vue {
    @Prop() images!: string[]|null; 
    public mainpic: null|string = null;

    mounted() {
        this.mainpic = this.images![0];
    }

    changeImg(img: string) {
        this.mainpic = img;
    }
}
</script>