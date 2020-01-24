<template>
    <form action="">
        <fieldset class="m-searchbar">
            <div class="m-input -text">
                <input placeholder="Search something" type="text" id="search">
                <label for="search"></label>
            </div>
            <div class="m-input -submit">
                <input type="submit" value="Search" class="a-button -primary">
            </div>
        </fieldset>
    </form>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Searchbar extends Vue {
    
}
</script>