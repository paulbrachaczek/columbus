<template>
    <nav class="m-menu">
        <div class="container">
            <ul>
                <li><a href="#">All our products</a></li>
                <li><a href="#">Inspiration for the office</a></li>
                <li><a href="#">About OS</a></li>
            </ul>
        </div>
    </nav>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Menu extends Vue {
    
}
</script>