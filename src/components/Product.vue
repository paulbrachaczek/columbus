<template>
    <div class="m-product" itemscope itemtype="http://schema.org/Product">
        <div class="m-product__top">    
            <Slider :images="product.images" />
            <div class="m-product__details">
                <h2 itemprop="name">{{product.name}}</h2>
                <fieldset class="m-product__add-to-cart">
                    <p class="m-product__price">
                        <b itemprop="price">{{product.price}} kr</b>
                        {{product.oldprice}} kr
                    </p>
                    <div class="m-input -select">
                        <select name="" id="">
                            <option :value="{color}"  v-for="(color, index) in product.colours" :key="{index}">{{color}}</option>
                        </select>
                    </div>
                    <button @click.prevent="update(product.price)" class="a-button">Buy</button>
                </fieldset>
                <div class="m-product__desc" v-html="product.desc"></div>
                <p v-if="!readmore">
                    <span @click="readmore = true" class="-read-more">read more</span>
                </p>
                <div v-if="readmore" v-html="product.more"></div>
            </div>
        </div>
        <div class="m-grid">
            <div class="m-grid__col" v-for="(card, index) in product.cards" :key="index">
                <div class="box">
                    <b>{{card.title}}</b>
                    <p>
                        {{card.text}}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { Component, Vue, Emit } from "vue-property-decorator";
import Slider from './Slider.vue';

@Component({
  components: {
    Slider
  }
})
export default class Product extends Vue {
    public product = {
        name: 'Paper',
        price: 55,
        oldprice: 60,
        desc: '<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.</p><p>Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</p><p>Nam fermentum, nulla luctus pharetra vulputate, felis tellus mollis orci, sed rhoncus sapien nunc eget odio.</p>',
        more: '<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.</p></p><p>Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</p>',
        colours: ['pink','red','blue','white'],
        cards: [
            {
                title: 'Paper is awesome',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nam fermentum, nulla luctus pharetra vulputate, felis tellus mollis orci, sed rhoncus sapien nunc eget odio.'
            },
            {
                title: 'Paper is awesome',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.'
            },
            {
                title: 'Paper is awesome',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. '
            }
        ],
        images: [
            'paper1.jpg', 'paper2.jpg', 'paper3.jpg'
        ]
    };
    public readmore = false;

    @Emit()
    update(price: number) {
        return price;
    }
}
</script>