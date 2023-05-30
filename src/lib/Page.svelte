<script>
import { products } from './products.svelte'

</script>
<main>
{#if products.length > 0}
{#each products as product}
    <div id="item">
        <div>
        <img src={product.img} alt="">
        </div>
        <div>
            <h3>{product.name}</h3>
            <h4>${product.price}</h4>
            <div class="add-to-cart">
                <input type="checkbox" id="fnt" bind:value={product.bought}/>
                <button ><label for="fnt">Add to Cart</label></button>
            </div>
        </div>
    </div>
    <div>
</div>

{/each}
{:else}

<div class="empty">Shopify Products are unavailable! Check Back Later!</div>
{/if}



</main>

<style lang="css">
.empty{
    text-align:center;
    margin-top:23px;
}
      main{
        display:flex;
        flex-direction:row;
        margin-bottom:100vh;
      }

    h4{
        font-family:Noto Sans Mono;
    }
    input{
        display:none;
    }
    #item{

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

       img{
            margin-top:40px;
            height:350px;
            width:350px;
        }
    @media (max-width: 800px){
          main{
        display:grid;
        place-items:center;
        text-align:center;
    }
        img{
            margin-top:40px;
            height:350px;
            width:350px;
        }
    }

</style>