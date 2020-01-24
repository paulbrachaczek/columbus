<template>
    <main class="o-main">
        <div class="container">
            <AsideMenu/>
            <Product @update="update"/>
        </div>
    </main>
</template>

<script lang="ts">
import { Component, Vue, Emit } from "vue-property-decorator";
import AsideMenu from './Aside.vue';
import Product from '../components/Product.vue';

@Component({
  components: {
    AsideMenu,
    Product
  }
})
export default class  Main extends Vue {   

    @Emit()
    update(price: number) {
        return price;
    }
}
</script>