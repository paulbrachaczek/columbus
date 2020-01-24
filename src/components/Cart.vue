<template>
    <div class="m-cart">
        <p class="icon-basket"><span class="m-cart__items">{{items}} st</span> <span class="m-cart__totalprice">{{summary}} kr</span></p>
        <a href="#" class="a-button -primary">Cart</a>
    </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Cart extends Vue {
    @Prop(Number) items!: number;
    @Prop(Number) summary!: number;
}
</script>