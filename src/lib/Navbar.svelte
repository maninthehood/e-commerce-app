<script>
import productLength from './Page.svelte'
</script>
<main>
<nav>
    <ul>
        <li>Shopify</li>
        <li><img src="https://img.icons8.com/?size=1x&id=13014&format=png" alt="cart image"></li>
    </ul>
</nav>

</main>

<style>

    *{
        margin:0;
        padding:0;
    }
    span{
        position: absolute;
        top:0;
        border-radius:999999px;
    }
    nav{
        color:white;
        padding:5px;
        height:50px;
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