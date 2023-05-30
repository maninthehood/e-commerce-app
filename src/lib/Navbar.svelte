<script>
import {toggleCart} from './Cart.svelte'

</script>

<main>
<nav>
    <ul>
        <li><a href="Cart.svelte">Shopify</a></li>
        <li on:click={toggleCart}><img src="https://img.icons8.com/?size=1x&id=13014&format=png" alt="cart"></li>
    </ul>
</nav>

</main>

<style>
    a{
        text-decoration:none;
        color:inherit;
        transition:500ms;
    }
    a:hover{
        color:green;
        transition:500ms;
    }
    *{
        margin:0;
        padding:0;
    }
    nav{
        color:white;
        padding:5px;
        height:80px;
        box-shadow:1px -5px 26px 10px blue;
    }
    ul{
        display: flex;
        position: relative;
    }
    li:nth-child(1){
        font-size:30px;
        margin-right:auto;
        padding-top:20px;
        padding-left:20px;
    }
    li:nth-child(2){
        padding-top:3%;
    }
    ul>li{
        list-style-type: none;
    }
    img{
        width:50px;
        height:50px;
    }
</style>