<script>

 let products = [
  {
    id: 1,
    name: 'Iphone 14 Pro Max',
    img: 'https://fdn2.gsmarena.com/vv/pics/apple/apple-iphone-14-pro-max-1.jpg',
    price: 999,
    bought: false,
  },
  {
    id: 2,
    name: 'Iphone 13 Pro Max',
    img: 'https://www.apple.com/newsroom/images/product/iphone/standard/Apple_iphone13_hero_09142021_inline.jpg.slideshow-xlarge_2x.jpg',

    price: 599,
    bought: false,
  },
  {
    id: 3,
    name: 'Iphone 12 Pro Max',
    img: 'https://m.media-amazon.com/images/I/71XXJC7V8tL.jpg',
    price: 899,
    bought: false,
  },
];
let showCheckout = false;
  export function toggle() {
      alert("Checkout being rendered")
    showCheckout = !showCheckout;
  }
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
                <input type="checkbox" id="fnt" bind:value={product.bought}/>
                <button ><label for="fnt">Add to Cart</label></button>
            </div>
        </div>
    </div>
    <div>
</div>

      {#if showCheckout}
        <div class="checkout">
          <div class="checkout-title">
            <h2>Checkout</h2>
          </div>
          <hr />
          <div class="checkout-items">
            {#each products as cartItem}
              {#if cartItem.bought}
                <div class="cart-item">
                  <img class="cart-img" src={cartItem.img} alt="cart" />
                  <div
                    style="border-left:1px solid #000;height:100px;margin-right:1rem;margin-left:1rem;"
                  />
                  <p>Price:</p>
                  <p>{cartItem.price}</p>
                </div>
                <hr/>
              {/if}
            {/each}
          </div>
        </div>
      {/if}
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
        display:none;
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