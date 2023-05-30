<script>
import Navbar from './Navbar.svelte'
import products from './products.svelte'

</script>
<main>
{#each products as product}
    <div>
        <div>
        <img src={product.img} alt="">
        </div>
        <div>
            <h3>{product.name}</h3>
            <h4>${product.price}</h4>
            <div class="add-to-cart">
                <input type="checkbox" id="fnt"bind:value={product.bought}/>
                <!-- <button ><label for="fnt">Add to Cart</label></button> -->
            </div>
        </div>
    </div>
    <div>
    {product.bought}
</div>
{/each}


</main>

<style>
    main{
        margin-bottom:100vh;
        display:grid;
        place-items:center;
        text-align:center;
    }
    h4{
        font-family:Noto Sans Mono;
    }
    input{
        /* display:none; */
    }
    button{
        cursor: pointer;
        padding:10px;
        width:123px;
        border:none;
        background:#3A0CA3;
        color:white;
        border-radius:20px;
        transition:400ms;
    }
    button:hover{
        background:#003049;
        transition-duration:400ms;
        transform: translateY(5px)
    }
    button:active{
        background:#4F772D;
        color:black;
        transform: scale(1.1)
    }

    @media (max-width: 800px){
        img{
            margin-top:40px;
            height:350px;
            width:350px;
        }
    }

</style>