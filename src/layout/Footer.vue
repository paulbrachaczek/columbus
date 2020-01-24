<template>
    <footer class="o-footer">
        <div class="container">
            <div class="m-grid">
                <div class="m-grid__col -col-6">
                    <h1 class="a-logo">
                        <a href="#">
                            <figure class="a-figure">
                                <img alt="OfficeSupplies" src="@/assets/images/logo.svg" /> 
                            </figure>
                        </a>
                    </h1>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis molestias expedita exercitationem quam unde optio, quae soluta dignissimos laboriosam sunt temporibus omnis nulla esse maiores fuga magnam. Minus quae expedita dolores perspiciatis dicta, eos commodi ut velit aut qui recusandae unde, ipsa suscipit rerum.
                    </p>
                </div>
                <div class="m-grid__col">
                    <b>Bestsellers</b>
                    <ul>
                        <li><a href="#">A4</a></li>
                        <li><a href="#">A4</a></li>
                        <li><a href="#">A4</a></li>
                        <li><a href="#">A4</a></li>
                        <li><a href="#">A4</a></li>
                        <li><a href="#">A4</a></li>
                    </ul>      
                </div> 
                <div class="m-grid__col">
                    <b>Social</b>
                    <ul>
                        <li><a class="icon-facebook" href="#">Facebook</a></li>
                        <li><a class="icon-twitter" href="#">Twitter</a></li>
                        <li><a class="icon-linkedin" href="#">Linkedin</a></li>
                    </ul>
                </div>      
            </div>
        </div>
    </footer>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Footer extends Vue {
    
}
</script>