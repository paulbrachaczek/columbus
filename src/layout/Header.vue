<template>
    <header class="o-header">
        <div class="container">
            <button class="hamburger hamburger--squeeze" @click="active=!active" :class="{'is-active':active}">
                <span class="hamburger-box"><span class="hamburger-inner"></span></span>    
            </button> 
            <Logo/>
            <Searchbar/>
            <Cart :items="items" :summary="summary"/>
        </div>
        <Menu/>
    </header>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";
import Logo from './Logo.vue';
import Menu from './Menu.vue';
import Searchbar from '../components/Searchbar.vue';
import Cart from '../components/Cart.vue';

@Component({
  components: {
    Logo,
    Searchbar,
    Menu,
    Cart
  }
})
export default class Header extends Vue {
    @Prop(Number) items!: number;
    @Prop(Number) summary!: number;
    public active = false;
    
}
</script>